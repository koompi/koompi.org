---
title: "Basic Linux Commands"
date: 2018-12-28T11:02:05+06:00
icon: "ti-files"
description: "This section is available only the command lines supported in the open source world. "
type : "docs"
---

On KOOMPI OS, Some commands are using in the same way like other open-source operating system but some commands are new and has been using in the different way with the required of users.

All the tools and commands are down here. In addition, more information on how the team has produced in recent years is available. [Click here for the latest news](#).

## Pacman Or Pi Info
The *pi* that is **Pacman's shortcut** is one of our system's primary most efficient commands. It is a combination of the easy-to-use open-source system and the simple binary package manager.

We can install `pacman or pi packages` on the system with `pix`, here is the command:
```
pix i pi
```

{{< notice info >}}
If you don't know how to install pix, [Click here](#).
{{< /notice >}}



**pi or pacman** has used in many forms. All the details will be described in detail down below:
``` 
pi
pi <operation> [...]
pi <package(s)>
```

{{< notice note >}}
Packages also have optional modules, which are packages that do not actually allow the program to run. The list of optional package dependencies will be up when the package is installed.
{{< /notice >}}

{{< notice warning >}}
While you are installing packages, avoid refreshing the packages list without updated the system. In practice for running command do not run **$ pi -Sy package_name** instead of  **$ pi -Syu package_name**, as it could lead to dependency issues.
{{< /notice >}}

## Update Operating System with pi
The **mandatory step** is to upgrade your operating system before downloading any new applications.
```
 pi -Syu
```
For Database Updates:
```
pi -Syy
```
----
----