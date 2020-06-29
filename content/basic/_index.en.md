---
title: "Basic Commands"
date: 2018-12-28T11:02:05+06:00
icon: "ti-files"
description: "All available command lines supported in the open-source world "
type : "docs"
---
This section gives you the basic commands to keep your system up and running. Keep in mind that these commands can both install packages from any open-source repository and packages from the AUR.

As KOOMPI OS is operating base on Arch Linux and Plasma. This means your system always receives the latest packages.

----

## Pi or Pacman
The `pi` that is **Pacman's shortcut** is one of our system's primary most efficient commands. It is a powerful tool at the center of the system, that allows you to maintain, expand, and update the system.

Since you installed the operating system, `pi command` has always been installed, but We can also install `pacman or pi packages` on the system with `pix`. Here is the command:
```
 pix i pi
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

## Refreshing mirrors
Sometimes it can happen that your system can’t find the updates or packages. In that case, there’s a problem with the mirrors you’re trying to connect to. You can simply refresh the mirrors with this command.
```
 pi -Syyu
```

----
