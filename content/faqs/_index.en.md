---
title: "FAQs"
draft: false
date: 2018-12-26T11:02:05+06:00
icon: "ti-help-alt"
description: "Solutions and Problems that happened in the OS have been noted here."
type : "docs"
---

{{< faq "How to install KOOMPI OS?" >}}
In order to install KOOMPI OS, you need to click the link below which is the source of the OS. And it will be download somewhere in your folder. Copy that source code and make it as booted drive. After that input your dive in to the pc you want to install while you were
{{</ faq >}}

{{< faq "When will new version of KOOMPI OS release?" >}}
All Announcement about releasing the new version of KOOMPI OS will be announced in [KOOMPI Telegram Community](https://t.me/koompi). And it will be informed on new release section on the www.koompi.org](https://www.koompi.org/release/) as well.
{{</ faq >}}

{{< faq "How to update the system in KOOMPI OS?" >}}
In KOOMPI OS, You can update the system by using the Konsole or command line tools and a command like this.  
```
pi -Sy
```
{{</ faq >}}

{{< faq "Is KOOMPI OS is free to use?" >}}
KOOMPI OS  is the `free open-source software`, it is free to use as much as everyone like it. KOOMPI OS is fully customized and self-customizable which make it more special.
{{</ faq >}}

{{< faq "What is pi ?" >}}
The `pi` which is the shortcut formation of `pacman` is one of the majority features of our System. It is a combination of simple binary package manager with the easy-open-source-to-use build system.

If you want to know more details [click here]().
{{</ faq >}}

{{< faq "What is sudo ?" >}}
**sudo** — A widely used command in the Linux command line, sudo stands for "SuperUser Do". So, if 
you want any command to be done with administrative or root privileges, you can use the sudo 
command.

If you want to know more details [click here]().
{{</ faq >}}

{{< faq "What is different between pi and pix ?" >}}
As you know that pi is the shortcut form of pacman which we are using it to install applications and 
packages. Even though we had some updates we still using pi as the main command. 

Pix sounds familiar, but it is quite different because it stands for **pacman extended or extra** which is supported by many more applications.., etc. that **Pi** can't support like Microsoft office. 
{{</ faq >}}

{{< faq "How to install pi or pacman" >}}
you can install pi or pacman by pix command, to do so 
```
pix i pi
```
{{</ faq >}}

{{< faq "What is terminal or konsole ?" >}}
Originally, a konsole was a terminal “plugged into” the computer: it provided the interface that was 
used to configure and control the computer and to view messages from the operating system.

When a Linux server first boots, it prints status messages to the console, the familiar scroll of text that brings joy to many a Linux user. When you interact with your server, you connect a terminal to a program running in a console.
{{</ faq >}}

{{< faq "How to install applications in KOOMPI OS ?" >}}
In order to install the application in KOOMPI OS, you have to use commands in terminal or Konsole:
**Sample:**
```
 pi -S Package_Name
```

Please, click [here](https://www.koompi.org/applications/) for more info.
{{</ faq >}}


{{< faq "How to Change password in KOOMPI OS ?" >}}
As a KOOMPI OS or Linux system administrator (sysadmin) you can change the password for any users on 
your server. To change a password on behalf of a user:

1. First, sign on or “`su`” or “`sudo`” to the “`root`” account on **Pionux**, run: `sudo -i`
1. Then type, `passwd Administrator_name` to change a password for Admin user
1. The system will prompt you to enter a password twice.


For more info about password: [Click here]()
{{</ faq >}}

{{< faq "Conflicting python-pyqt5 and pyqt5-common, How to fix it ?" >}}
If you run command to update the system and facing erro like below:
```Text
 :: Synchronizing package databases...
 The core is up to date
 extra is up to date
 community is up to date
 :: Starting a full system upgrade...
 :: Replace ilmbase with extra/openexr? [Y/n] 
 :: Replace libmagick with extra/imagemagick? [Y/n] 
 :: Replace pygobject2-devel with extra/python2-gobject2? [Y/n] 
 resolving dependencies...
 looking for conflicting packages...
 :: python-pyqt5 and pyqt5-common are in conflict. Remove pyqt5-common? [y/N] 
 error: unresolvable package conflicts detected
 error: failed to prepare transaction (conflicting dependencies)
 :: python-pyqt5 and pyqt5-common are in conflict
 Error installing repo packages
```
In order to solve this problem, you have to run this command and follow all instuctions have been given.
```
sudo pacman -Rdd pyqt5-common
```
{{</ faq >}}
{{< faq "Still having Conflict with python-pyqt5 and pyqt5-common, How to fix it ?" >}}

You need to run this other command
```
sudo pacman -Rdd libdmx libxxf86dga
```
After that is done, run the updated command:
```
pi -Syu
```
After update just does this next command, you will be finished:
```
pacman -Rns $(pacman -Qqtd)
```
{{</ faq >}}

{{< faq "Missing Qt5 dependency, How to install it back ? " >}}
If you accidentally delete QT5 dependency you can install it back by:
```
pi -S qt5-base

```
{{</ faq >}}

{{< faq "How To Fix “invalid or corrupted package (PGP signature) ? " >}}
I tried to upgrade my Arch Linux server using the command `sudo pacman -Syu`, and You got the 
following error:
```
[...]
:: File /var/cache/pacman/pkg/libpsl-0.16.1-1-x86_64.pkg.tar.xz is corrupted (invalid or 
corrupted package (PGP signature)).
Do you want to delete it? [Y/n] y
error: failed to commit transaction (invalid or corrupted package)
Errors occurred, no packages were upgraded.
```
Even you try other commands like `$ pi -Syyu`, It still got the same error. To fix this issues one for all you 
have to update key-ring packages that following by command below:
```
sudo pacman -S archlinux-keyring
```
{{< notice info >}}
The above command will update the new keys and disable the revoked keys.
{{< /notice >}}
{{</ faq >}}


