---
layout: post    
title:  "C basics: Dynamic Libraries"
date: 2020-05-04 00:00:00 #YYYY-MM-DD HH:MM:SS

categories: [C basics]
tags: [C (programming language)]

image: /assets/img/posts/2020-05-04-c-basics-dynamic-libraries/banner.jpg
---

Today we will talk about dynamic libraries, what they are, how they work and what is the difference between static and dynamic libraries.

First of all we must know that it is a library, for which I recommend to see my previous article "[C basics: Static Libraries.](/posts/c-basics-static-libraries)", in which the concepts of static libraries are deepened, as a review:

## **¿What is a static library?**

A static library is a library that "copies" itself into our program when we compile it. Once we have the executable of our program, the library is useless. We could delete it and our program would still work, since it has a copy of everything it needs.

Taking into account the concept seen above we can give way to the dynamic libraries.

## **¿What is a dynamic library?**

Are libraries that are loaded into the application at runtime. When you compile a program that uses a dynamic library, the library does not become part of your executable but remains a separate unit.

### **How to create a dynamic library**

Once we have our code, in order to get a static library we must perform the following steps:

1. Obtain the object files (.o) from all our sources (.c), Object files for the dynamic library need to be compiled with the -fPIC flag (PIC = position independent code).

```bash
gcc -c -fPIC source.c -o source.o
```

2. Create the library (.so). To do this, use the command ar with the following parameters:

```bash
gcc -shared object-file.o -o liball.so
```

3. As long as the shared library is not installed in a default location (such as /usr/lib), we must indicate where it is found. This is possible with the LD_LIBRARY_PATH environment variable:

```bash
LD_LIBRARY_PATH="path-of-the-file"
```

Now you can use your dynamic libary.

## **But, ¿why use libraries?**

The value of a library lies in its reusability. When a program invokes a library, it gets the behavior implemented within that library without having to implement that behavior itself. Libraries make it easier to distribute the code.

## **¿What is the difference between static and dynamic libraries?**

The main difference between the dynamic libraries and the static libraries is that the static libraries are copied with the executable and the dynamic ones are compiled when the program is executed, the best way to illustrate this is with a reference image:

![example1](/assets/img/posts/2020-05-04-c-basics-dynamic-libraries/example1.jpg)

## **¿What are the advantages and drawbacks of each of them?**

One advantage of dynamic libraries is that many programs can share one copy, which saves space. Perhaps a bigger advantage is that the dynamic library can be upgraded to a newer version without replacing all of the executables that use it.

One advantage of the static libraries is that when they are implemented in the program it does not matter if the original components are deleted because inside the executable there is a copy of it, however if a dynamic library is removed the program could not be executed because it depends directly on the integrity of the file containing the library.

Another advantage of the dynamic libraries is that they are lighter than the static ones, because they take up more space.

Finally, the runtime speed in the static libraries is faster because your code is in the executable file, as opposed to the dynamics which have their code out.

---
I hope this information has been to the liking of all the viewers, and **RTFM** :)