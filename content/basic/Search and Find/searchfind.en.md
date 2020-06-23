---
title: "Search/ Find"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---
In this tutorial we'll look at the `find` command and how you can quickly use it to **locate** files in your filesystem. Find is a powerful utility capable of locating files anywhere on your system including mounted drives and removable storage, processing regular expressions, and even running other commands on those files. Fortunately only a few simple options are needed to provide most users with all the capability they need.


The `find` command is a command line utility for walking a file hierarchy. It can be used to find files and directories and perform subsequent operations on them. It supports searching by file, folder, name, creation date, modification date, owner and permissions. 



### Find File By Name
As with most open-source commands, you have a number of available options. And we are attempting to find a file by name, we’ll use one of two options:

+ **name** – case sensitive
+ **iname** – case insensitive

Remember, Open-source is very particular about case, so if you’re looking for a file named Linux.odt, the following command will return no results.
```
sudo find / -name filename.extension
```
Sample:
```
sudo find / -name text.txt
```
If, however, you were to alter the command by using the -iname option, the find command would locate your file, regardless of case. So the new command looks like:
```
sudo find / -iname filename.extension
```