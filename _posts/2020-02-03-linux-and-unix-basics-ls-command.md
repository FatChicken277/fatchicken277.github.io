---
layout: post    
title:  "Linux and Unix basics: Ls Command"
date: 2020-02-03

categories: [Linux and Unix basics]
tags: [linux]

image: /assets/img/posts/2020-02-03-linux-and-unix-basics-ls-command/banner.png
---

In this post we will see basic of the command “ls” and what happens if we put “ls *.c”, but before we do thiswe have to know what the “ls” command is and what it’s for:

## **What is ls command?:**

The “ls” command is a program of the shell he will show a directory contents on a list.

## **How ls command works?:**

The “ls” command can be executed only typing “ls” on terminal generating as a result the display of files and directories ofthe current path on a list.

<div align="left">
    <img alt="example1" src="/assets/img/posts/2020-02-03-linux-and-unix-basics-ls-command/example1.png">
</div>

In the previous image we can see that when we put the command “ls” all the existing files in the example folder are listed.

the “ls” command has a certain number of parameters to change the result of the list, the most common are :

- `ls -l` use a long listing format.
- `ls -a` do not ignore entries starting with “.” (show the hidden files).
- `ls -R` list subdirectories recursively.

There are many more ([see more](https://ibb.co/C8HJ05d)), but I think these are the most significant, taking into the above, if we want to list the files in a long way and taking into the hidden files, What should we do?.

<div align="left">
    <img alt="example2" src="/assets/img/posts/2020-02-03-linux-and-unix-basics-ls-command/example2.png">
</div>

as we can see, adding the “a” and “l” parameters to the “ls” command will list the files long and show the hidden files.

Taking into this important information we can we can now explain the question at the beginning

## **What do the command “ls *.c” ?:**

Now that we know what the “ls” command does, we need to know what “*.c” is for.

the `*` means all, so if we put something in front of the `*` in the following way “n*” means that any file containing an “n” character at the beginning will be listed:

<div align="left">
    <img alt="example3" src="/assets/img/posts/2020-02-03-linux-and-unix-basics-ls-command/example3.png">
</div>

Similarly, if we put something after the `*` it means that any file containing an “n” character at the end will be listed:

<div align="left">
    <img alt="example4" src="/assets/img/posts/2020-02-03-linux-and-unix-basics-ls-command/example4.png">
</div>

So the structure of the command “ls *.c” it means that anything ending in .c will be listed:

<div align="left">
    <img alt="example5" src="/assets/img/posts/2020-02-03-linux-and-unix-basics-ls-command/example5.png">
</div>

Finally we can vary the previous command and any other with the parameters seen before at the beginning of the blog.

I hope this information has been to the liking of all the viewers, and **RTFM** :)
