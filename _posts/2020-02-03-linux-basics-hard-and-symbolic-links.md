---
layout: post    
title:  "Linux basics: Hard & Symbolic links"
date: 2020-02-03 11:22:00 #YYYY-MM-DD HH:MM:SS

categories: [Linux basics]
tags: [Linux]

image: /assets/img/posts/2020-02-03-linux-basics-hard-and-symbolic-links/banner.jpg
---

In this blog we will see the concepts of link (symbolic and hard), what they are for and how each one works, but first we must know what a link is so:

## **What is a link?:**

A link is a connection between a file and the actual data on the disk. Links are a very handy way to create a shortcut to an original directory.

a less technical but clearer definition could be a link is created to connect to any other file on the hard drive so we don't have to look for the original file every time we have to use it

Once created, a link can be used in place of the target file name. It can have a unique name, and be located in any directory. Multiple symbolic links can even be created to the same target file, allowing the target to be accessed by multiple names.

**There are two types of links :**

1. Soft Link or Symbolic links
2. Hard Links

## **Hard Links:**

hard links, can only link to files (and not directories); you cannot reference a file on a different disk or volume, and they reference the same inode as the original source. A hard link will continue to remain usable, even if the original file is removed.

1. Each hard linked file is assigned the same value as the original, therefore they reference the same physical file location. Hard links more flexible and remain linked even if the original or linked files are moved throughout the file system.
2. Links have actual file contents
3. Removing any link, just reduces the link count, but doesn’t affect other links.
4. If original file is removed then the link will still show the content of the file.

**How to create a hard link**
```bash
ln <original filename> <link name>
```

## **Soft Links:**

soft link, reference a file/folder on a different disk or volume, will exist as a unusable link if the original location is deleted, soft links too reference abstract filenames and directories, and are given their own, unique inode.

1. Soft Link contains the path for original file and not the contents.
2. Removing soft link doesn’t affect anything but removing original file, the link becomes “dangling” link which points to nonexistent file.
3. A soft link can link to a directory.

**How to create a soft link**
```bash
ln -s <original filename> <link name>
```

## **Conclusion:**

To conclude we can say that the clearest difference between the types of links is:

- **Hard Link:** Refer to the specific location of physical data.

- **Symbolic Link:** Refer to a symbolic path indicating the abstract location of another file.

![example1](/assets/img/posts/2020-02-03-linux-basics-hard-and-symbolic-links/example1.png)

---
I hope this information has been to the liking of all the viewers, and **RTFM** :)