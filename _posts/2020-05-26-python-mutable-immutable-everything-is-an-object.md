---
layout: post    
title:  "Python: Mutable, Immutable... Everything is an object!"
date: 2020-05-26 00:00:00 #YYYY-MM-DD HH:MM:SS

categories: [Python]
tags: [Python]

image: /assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/banner.png
---

Today we will talk about classes and objects, which are and also which are the mutable and immutable objects but first of all...

## **What is a class**

A class creates a new type where the objects are instances of the class. Defines the properties and behavior of a particular object type.

Instantiation is the reading of these definitions and the creation of an object from them.

To create a class in python you have to start with the keyword "class" followed by the class name as follows:

![example1](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example1.png)

Now that we know it's a class we can go on with the definition of object, so...

## **What is an object**

It's an instance to a class.

Entity provided with a set of properties or attributes (data) and behavior or functionality (methods), which consequently react to events. They correspond with the real objects of the world around us, or with internal objects of the system (of the program). example:

![example2](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example2.png)

Now that we know what the objects are, it's important to know what the attributes are, so...

## **What is an attribute**

Attributes are like properties that we want to add to the class (type).

For example, for our "Person" class, we're going to add two attributes: "name" and "id":

![example3](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example3.png)

The last but not least concept is that of method so again...

## **What is a method**

Algorithm associated with an object (or a class of objects), whose execution is triggered by the receipt of a "message". From a behavioral point of view, this is what the object can do. A method can produce a change in the object's properties, or the generation of an "event" with a new message for another object in the system.

### **Class method**

Class methods only have one specific difference from ordinary functions: they must have an additional name that must be added to the beginning of the paramet   er list, but it does not give a value for this parameter when you call the method, Python will provide that. This particular variable refers to the object itself and, by convention, is given the name "self". Example:

![example4](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example4.png)

Now that we know the basic concepts about classes and objects we can proceed

### **Id and type methods**

* **type()** method returns class type of the argument(object) passed as parameter. type() function is mostly used for debugging purposes. example:

![example5](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example5.png)

* **id()** return the “identity” of an object. This is an integer (or long integer) which is guaranteed to be unique and constant for this object during its lifetime. example:

![example6](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example6.png)

## **Mutable objects and immutable objects**

Python objects can be mutable or immutable

### **Inmutable objects**

immutable objects in python are numerical objects such as integers, floats and booleans, as well as strings and tuples.

These objects when created will always be created in different memory spaces, we can see this with an example using the function id():

![example7](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example7.png)

although we can easily get confused with the creation of objects, because new objects are not always created, since in python two objects with non-overlapping lives can have the same id() value to save resources. example:

![example8](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example8.png)

### **Mutable objects**

mutable objects in python are ready-made data structures, sets and dictionaries.

These objects unlike the immutable are more complex because they work with the theme of pointers which makes them special because it allows the optimization of resources because it can change in the future once stored in a memory position and if you have to use the same object always pointed from different variables. example:

![example9](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example9.png)

## **How arguments are passed to functions and what does that imply for mutable and immutable objects**

### **Inmutable objects**

When the unchanging value is passed as a parameter to a function, it is immediately copied to another address in memory. Therefore, what happens inside the function will remain inside the function and will not affect variables outside the function (unless it is returned with "return"). example:

![example10](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example10.png)

### **Mutable objects**

when a mutable object is passed as an argument to a function, the opposite happens as with immutable objects, because this time a copy of the object is not created and the value will be affected. example:

![example11](/assets/img/posts/2020-05-26-python-mutable-immutable-everything-is-an-object/example11.png)

## **Why does it matter and how differently does Python treat mutable and immutable objects**

It is important to take into account how mutable and immutable objects work because, depending on the needs, one or the other is good

immutable objects are used more when you need to work with objects that you need to keep intact, or if you need copies of them, even if this entails more resource usage.

On the contrary, mutable objects are better when you need to work with more data that is also frequently updated, without the need to generate copies, which implies a lower use of resources.

**And with this last one we finish today's topic, I hope that this information was of great help.**

---
I hope this information has been to the liking of all the viewers, and **RTFM** :)