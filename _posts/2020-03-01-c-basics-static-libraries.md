---
layout: post    
title:  "C basics: Static Libraries"
date: 2020-03-01 00:00:00 #YYYY-MM-DD HH:MM:SS

categories: [C basics]
tags: [C (programming language)]

image: /assets/img/posts/2020-03-01-c-basics-static-libraries/banner.png
---

In this post we will see what the C static libraries are but before that we must know what a library is:

## **What is a library?**

Libraries are a group of files that have a functionality, and that can be used by any executable. Libraries contain variables and functions inside them, known as libraries to certain types of files that we can import or include in our program. 

a library is a file which contains a set of files that have a functionality, the libraries can be used as a single entity in a linking phase of a program. Linking a program whose files are arranged in libraries is faster than linking a program whose object files are separated on disk. Also, when we use a library, we have fewer files to search and open, which speeds up linking even more.

There are 2 types of libraries:

- Static libraries
- Dinamic libraries

In this case we'll only see the static libraries.

## **Static libraries**

A static library is a library that "copies" itself into our program when we compile it. Once we have the executable of our program, the library is useless (i.e., it serves other future projects). We could delete it and our program would still work, since it has a copy of everything it needs. Only the part of the library that you need is copied. For example, if the library has two functions and our program only calls one, only that function is copied.

an example of a static library may well be the standard c:

![example1](/assets/img/posts/2020-03-01-c-basics-static-libraries/example1.png)

### **How to compile and use a c program with static libraries**

Once we have our code, in order to get a static library we must perform the following steps:

- Obtain the object files (.o) from all our sources (.c) To do this they are compiled with gcc -c source.c -o source.o. The -c option tells the compiler not to create an executable, but only an object file.

```bash
gcc -c source.c -o source.o.
```

- Create the library (.a). To do this, use the command ar with the following parameters: ar -rc libnombre.a fuente1.o fuente2.o ... The -r option tells the ar command to insert (or replace if already inside) the object files in the library. The -c option tells ar to create the library if it does not already exist. 'r'. Then, we put all the object files we want.

```bash
ar -rc libname.a source1.o source2.o...
```

- After we create our file, we want to use it in a program. This is done by adding the library name to the list of object file names given to the linker, using a special flag, usually '-l'. Here is an example:

```bash
gcc main.c -L. -lname -o program.
```

This will create a program using the "main.c" file, and any symbols that require the static library "name". Note that we omitted the "lib" prefix and the ".a" suffix when mentioning the library in the link command. Note also the use of the '-L' flag: this flag tells the linker that the libraries can be found in the given directory ('.', Referring to the current directory)

---
I hope this information has been to the liking of all the viewers, and **RTFM** :)
