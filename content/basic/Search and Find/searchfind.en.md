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
Sample:
```
sudo find / -iname text.txt
```

### Find By Type
What if you’re not so concerned with locating a file by name but would rather locate all files of a certain type? Some of the more common file descriptors are:

|    Options| Description         | 
|:----------:|:--------------------|
| **f**     |      `Regular File` |
| **d**     |      `Directory`    |
| **l**     |      `Symbolic Link`|
| **c**     |      `Chracter Devices`|
| **b**     |      `Block Devices`|

Now, suppose you want to locate all `block devices` (a file that refers to a device) on your system. With the help of the `-type` option, we can do that like so:
```
sudo find / -type b
```

We can use the same option to help us look for configuration files. Say, for instance, you want to locate all regular files that end in the `.conf` extension. This command would look something like:
````
sudo find / -type  f -name "*.conf"
````
### Find Modified Files Since Last 60 minutes

```
find / -mmin -60
```
### Find Change Files Since Last 6 minutes

```
find / -cmin -60
```
### Find All Files Which Are Accessed 7 days
```
find / -atim 7
```
### Finding Files By Size
We can use the find command to locate files of a certain size. Say, for instance, you want to go large and locate files that are over **1000MB**. The find command can be issued, with the help of the `-size` option, like so:
```
find / -size +1000M
```
You can also find all files which are greater than or less than, too. For example, `( Greater than 10MB Less than 100MB )`
```
find / -size +10M -size -10M
```
With the output from the command, you can comb through the directory structure and free up space or troubleshoot to find out what is mysteriously filling up your drive.

You can search with the following size descriptions:

|    Options| Description         | 
|:----------:|:--------------------|
| **c**     |      `Bytes` |
| **k**     |      `Kilobytes`    |
| **M**     |      `Megabytes`|
| **G**     |      `Gigabytes`|
| **b**     |      `512-byte blocks`|

----