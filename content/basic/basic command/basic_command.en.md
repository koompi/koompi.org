---
title: "Basic"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---

This document is a guide for beginners who do not know anything about the command lines. All the basic command lines will be provided here with the explaination plus the example.

For more details instruction, see the [KOOMPI OS website](www.koompi.org) articles or the various [program section](www.koompi.org/applications/), both linked from this guide.

Basic commands should be all run on the konsole, terminal or command line tools. If you could not find anything related to what you are looking for, submit the question.

---
---

## Pwd Command
To show the directory you are currently in:
```
 [koompi@koompi-pc ~]$ pwd
```
**Output :**
```
 /home/koompi
```
---
---
## Ls Command
Use "ls" for showing all the files in your directory:
```
 [koompi@koompi-pc ~]$ ls
```
Output :
```
Desktop         Save            dconf           
Documents       Videos          Downloads code 
Musics          example.desktop mkrepo 
```
Use "ls -a" to list down even the hidden files:
```
 [koompi@koompi-pc ~]$ ls -a
```
**Output :**
```
 .              ..          .mozilla    .viminfo
 .vscode-oss    Save        dconf       mkrepo 
 Desktop        Videos      Documents   Downloads 
 Musics         example.desktop code
```
---
---

## Cd Command
" cd " ― Use this command for go into other directory.If you are in /home/koompi you want go into 
*Documents*:
```
 [koompi@koompi-pc ~]$ pwd
 /home/koompi
 [koompi@koompi-pc ~]$ cd Documents/
```
Output :
```
 [koompi@koompi-pc Documents]$
```
## Touch Command
To create file " touch ":
```
touch <file name with extension >
```
**For example :**
```
touch Name.txt
```

---
---

## Mkdir Command
To create a directory, you must use:
``` 
mkdir <name of directory you want to put>
```
For removing the directory, you can use:
```
rmdir <name of directory you want to delete>
```
{{% notice note %}}
This command only working when your directory is empty.
{{% /notice %}}

---
---

## Rm Command
To delete directory or files, "rm" it is:
```text
rm <file's name or directory's name>
```
{{% notice tip %}}
we are Strongly not Recommended it.
{{% /notice %}}

{{% notice warning %}}
Not only empty directory or file, but also everything!!!
{{% /notice %}}
If you cant't delete, you can use command below to force remove:
```
rm -rf <directory or files's name>
```
Need some helps with commands, this would be useful:
```
man cd or $ cd --help
```
---
--- 
## Cd Command
(" cd ") is the command you might need to know more infomation.
Output :
```shell
cd: cd [-L|[-P [-e]] [-@]] [dir]
```
Change shell working directory.
Change the current directory to DIR. The default DIR is the value 
 OME shell variable.
 
The variable CDPATH defines the search path for the directory conta
DIR. Alternative directory names in CDPATH are separated by a colo
A null directory name is the same as the current directory. If DIR
with a slash (/), then CDPATH is not used.
 
If the directory is not found, and the shell option `cdable_vars' i
the word is assumed to be a variable name. If that variable has a
its value is used for DIR.

**Options:**
 - `L` force symbolic links to be followed: resolve symbolic
 links in DIR after processing instances of `..'
 - `P` use the physical directory structure without following
 symbolic links: resolve symbolic links in DIR before
 processing instances of `..'
 - `e` if the -P option is supplied, and the current working
 directory cannot be determined successfully, exit with
 a non-zero status
 - `@` on systems that support it, present a file with extende
 attributes as a directory containing the file attribute

The default is to follow symbolic links, as if `-L' were specified.
`..' is processed by removing the immediately previous pathname com
back to a slash or the beginning of DIR.

**Exit Status:**
 
Returning `0` if the directory is changed, and if $PWD is set successful:
```
 -P is used; non-zero otherwise.
```
---
---
## Cp Command
"Cp", You know, you can also copy file through command. It takes only two arguments: The first is the location of the file to be copied, the second is where to copy.
```shell
[koompi@koompi-pc ~]$ ls
Desktop            Save                    dconf               mkrepo
Documents          Videos                  Downloads code
Musics             example.desktop         New.txt
[koompi@koompi-pc ~]$ cp New.txt /Documents
```
Let's check in *Documents* directory:
```
[koompi@koompi-pc ~]$ ls Documents/
New.txt
```

---
---

## Mv Command
"mv" ― You know, you can also move file through command. It takes only two arguments like `cp`:
```shell
[koompi@koompi-pc ~]$ ls
Desktop    Save    dconf       mkrepo 
Documents  Videos  Downloads   code 
Musics     example.desktop     New.txt
[koompi@koompi-pc ~]$ mv New.txt /Documents
```
Here in **Documents** directory:
```
[koompi@koompi-pc ~]$ ls Documents/
New.txt
```
If you want to search for the locateion of the file, you can use **locate**:
```
locate <file_name>
```
---


----
----