---
title: "Basic Commands"
date: 2018-12-28T11:02:05+06:00
icon: "ti-files"
description: "This section is available only the command lines supported in the open-source world. "
type : "docs"
---
This section gives you the basic commands to keep your system up and running. Keep in mind that these commands can both install packages from any open-source repository and packages from the AUR.

As KOOMPI OS is operating base on Arch Linux and Plasma. This means your system always receives the latest packages.

----

## Pi or Pacman
The `pi` that is **Pacman's shortcut** is one of our system's primary most efficient commands. It is a powerful tool at the center of the system, that allows you to maintain, expand, and update the system.

Since you installed the operating system, `pi command` has always been installed, but We can also install `pacman or pi packages` on the system with `pix`. Here is the command:
```
 pix I pi
```

{{< notice info >}}
If you don't know how to install pix, [Click here](#).
{{< /notice >}}

----

## Update Operating System with pi
As I have mentioned above that the system always receives the latest packages, as long as you do the updating command.

The **mandatory step** is to upgrade your operating system before downloading any new applications.
```
 pi -Syu
```
For Database Updates:
```
 pi -Syy
```

----

## Searching packages
To search for packages in Pacman you can use the command
```
 pi -Ss package_name
```
When you’ve found the package you can install it according to the instructions in the paragraph here below.

{{< notice note >}}
When you can’t find the desired package, this means it isn’t in the KOOMPI OS repo, but you’ll find it most likely in the AUR. For searching and installing packages in the AUR we refer yo to the yay article.
{{< /notice >}}

---
## Installing Packages

Follow the following command to install a signal package including the dependencies:
```
 pi -S <Package name> or pi -i <Package name>
```
For the list of packages installation:
```
 pi -S <Package name1 Package name2 ...>
```
---

## Installing Package Group

Some packages belong to a **group of packages** that simultaneously call installation. As in here, for instance
```
 pi -S <Package group name>
```
To see what inside the package group, run
```
 pi -Sg <Package group name>
```

---

## Removing Packages
A package is always installed with other packages that it *depends on*, `called dependencies`. Quite often those dependencies are already, or partially installed on your system because other **packages also depend on it**.

If you just want to remove the package, the command following will be enough
```    
 pi -R <Package name>
```
If you rather want to avoid a `cluttered system` you can remove a package and its dependencies, without removing dependencies that are used by other installed packages, use the following command.

```
 pi -Rs <Package name>
```
To remove a package, its dependencies and all the packages that depend on the target package
```
 pi -Rsc <Package name>
```
For deleting a package that other packages need without deleting their dependency package

```
 pi -Rdd <Package name>
```



{{< notice note >}}
All operations have required a password. Then if you aren’t satisfied with the build tool and configuration choices, you can eject at any time. This command will remove the single build dependency from your operation.
{{< /notice >}}

{{< notice tip >}}
Here Special usage to automate the install procedure (Recommend):
{{< /notice >}}

```
 yes | pi -S <Package name> 
```
	
{{< notice tip >}}
Install packages with no confirm.
{{< /notice >}}

```
 pi -S --noconfirm <Package name>
```
## Refreshing mirrors
Sometimes it can happen that your system can’t find the updates or packages. In that case, there’s a problem with the mirrors you’re trying to connect to. You can simply refresh the mirrors with this command.
```
 pi -Syyu
```

----
