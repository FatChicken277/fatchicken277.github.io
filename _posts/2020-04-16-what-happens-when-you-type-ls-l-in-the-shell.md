---
layout: post    
title:  "¿What happens when you type ls -l in the shell?"
date: 2020-04-16 00:00:00 #YYYY-MM-DD HH:MM:SS

categories: []
tags: [Linux]

image: /assets/img/posts/2020-04-16-what-happens-when-you-type-ls-l-in-the-shell/banner.png
---

First of all I would like to explain why this question; During the creation of our own shell ([FLAME](https://github.com/RedLyon1200/simple_shell)) we realized the importance of the whole process involved in the inner workings of a shell, thanks to the experience this project has given us we would like to share some of our new knowledge. So let's start from the beginning:

## **¿What is a shell?**

> Simply put, the shell is a program that takes commands from the keyboard and gives them to the operating system to perform. ~*[Linuxcommand.org](http://linuxcommand.org/lc3_lts0010.php)*

With this definition in mind, we make our shell work as follows:

When the shell starts, it prints a message, with a defined format within the program code (promt). In this message, the user will have a place to enter a text string that will be the command and the arguments. Then, when pressing the "enter" key, the shell executes the command and prints the message again waiting for the next command.

![example1](/assets/img/posts/2020-04-16-what-happens-when-you-type-ls-l-in-the-shell/example1.jpg)

This cycle of asking the user, receiving a command/argument line, processing it and then asking the user again, continues infinitely until the user exits the shell through the "exit" command (or also through EOF

## **System calls**

System call **provides** the services of the operating system to the user programs via Application Program Interface(API).

They are the fundamental interface and communication between an application and the Linux kernel.

## **"ls -l"**

When the user enters the command "ls -l" and presses the "enter" key, the shell gets the line just entered through the "getline" function that stores the text entered. Once obtained, the program divides it into words taking into account a series of predefined delimiters and then analyzes them.

After this the shell takes the first parameter and treats it as the command and the following words will be taken as arguments.exm.

```console
FLAME -> $ ls -l
```

in this case "FLAME - >" will be the promt repeated in each interaction, "ls" will be the command and "-l" will be the argument.

Each command entered by the user is checked in a series of system directories described in the PATH variable to see if the command entered exists or not.

```console
PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin


/usr/local/sbin/ls          ✖️
/usr/local/bin/ls           ✖️
/usr/sbin/ls                ✖️
/usr/bin/ls                 ✖️
/sbin/ls                    ✖️
/bin/ls                     ✔️ <--
/usr/games/ls               ✖️
/usr/local/games/ls         ✖️
/snap/bin/ls                ✖️

```

After knowing if the program exists or not the next step is to know if the argument we have just entered is also valid, so the system call excve is in charge of executing the command with the argument, if it is valid it will be executed and if not, the shell will show a warning describing the problem.

If the program was executed successfully it will print as usual on the stdout (stdout, also known as standard output, is the default file descriptor where a process can write output.) and then repeat the cycle again until the user decides to stop it.

Each time a command is executed, the program (parent process) requires a child process (which is obtained through the "fork" function), which is in charge of executing the command. When the child process finishes executing it dies and the parent process repeats the sequence; it is important to take the processes into account because if they are not used the program will not work correctly since every time the system calls "execute" the process that calls it ends with it.

![example2](/assets/img/posts/2020-04-16-what-happens-when-you-type-ls-l-in-the-shell/example2.png)

Finally, we hope that this publication is to the liking of all its readers and that it has been useful to understand more about the process behind a projectile and all that is involved in the execution of a simple command. In addition, many of you can find in this publication a good source of information and advice in case you feel the need to understand the inner workings of command execution for a specific purpose.

And last but not least, since you already know what a shell is and have taken an interest in it, please feel free to stop by our [github repository](https://github.com/RedLyon1200/simple_shell) which contains more detailed information about our project.

---
I hope this information has been to the liking of all the viewers, and **RTFM** :)