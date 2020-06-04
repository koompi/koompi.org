---
title: "FAQs"
draft: false
date: 2018-12-26T11:02:05+06:00
icon: "ti-help-alt"
description: "Solutions and Problems that happened in the Operating System have been noted here."
type : "docs"
---
On this content, it provides to all questions and answers that have been facing in common. We hope that it helps the situations you are in . 

{{< notice info >}}
If there aren't any questions or answers you were looking for please contacts us. We are 
very happy about your request and participate in our community.
{{< /notice >}}
----
----
{{< faq " Error locale !!" >}}
Error locale is commonly seen. Sometimes, it can be seen while your time or date isn't correct with your location. So, the solution you can just reset the time or use this:
```
sudo locale-gen
```
{{< notice info >}}
While you are trying to reset automically your time, you must connect to internet.
{{< /notice >}}
{{</ faq >}}

{{< faq " How can I change default apps has been used ?" >}}
In general, After you have installed the OS each of the apps will choose their own default app which has been decided by developer but you can change it with the following steps:
1. you need to search for `System setting`.
1. After that, you have to find the `Applications` section.
1. Then, you will find the `Default Applications` layout.
1. Finally, Selecting the program you want it to change and applying it.

Sample: As my web browser has been using elinks as my default app, so I want to change it and using firefox instead. I follow the following step and in the `Default applications` section. I look for web browser and apply firefox instead of elinks. That's done. now I have used firefox as my deffault browser.
{{</ faq >}}

{{< faq "Zoom issue and can not run !!!" >}}
As the `ZOOM` is requiring the `QT5`, you can run the command below:
```
pi -S --noconfirm xz qt5-webengine zoom
```
After, Finish the command and zoom still not running, [Click here](#).
{{</ faq >}}

{{< faq "Can KOOMPI OS be able to install Spotify ?" >}}
Of Course, you can install it. [Visiting here to know how to install applications in KOOMPI OS](https://www.koompi.org/applications/).
{{< notice note >}}
As you know spotify is not available in some countries !!
{{< /notice >}}
{{</ faq >}}

{{< faq "Can KOOMPI OS run with IOS ?" >}}
In the meantime, our software isn't supporting the IOS system yet, but we are looking forward to doing it.
{{</ faq >}}

{{< faq "Can KOOMPI OS run Adobe Lightroom ?" >}}
In the meantime, We can’t run Lightroom in KOOMPI Operating yet, but many other applications have similar features and high quality as them. 

For example, GIMP which is supporting many works such as graphics editor, Image retouching and editing, free-form drawing, converting between different image formats, and more specialized tasks. 

For Adobe Lightroom, Our team is trying their best to bring it as much as possible.
{{</ faq >}}

{{< faq "Can KOOMPI OS run Adobe Photoshop ?" >}}
Not extacly, You can for some reasns. In order to install it, you need to instal `pix` first, [Click here](#).
{{</ faq >}}

{{< faq "How to install KOOMPI OS?" >}}
<!-- In order to install KOOMPI OS, you need to click the link below which is the source of the OS. And it will be download somewhere in your folder. Copy that source code and make it as booted drive. After that input your dive in to the pc you want to install while you were -->
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

{{< faq "Applications can not run, How to solve it ?" >}}
As your apps can not run, you might be facing error related to missing dependencies of the apps. In order to know, what kind of dependencies that your apps required. You need to run the keyword of the package name, and it  will show your missing dependencies.[Visit here to see all the dependencies](#).

Sample: I am facing with can not run **telegram app**. So, the keyword pacckages of telegram app is `telegram-desktop`. I run the keyword in konsole:
```
telegram-desktop
```
The output will be showing and you can see name of dependencies that are missing, mostly all apps are missing QT5, libicu. We can install dependency packages back by  run:
```
pi -S <Name of dependency packages>
```
{{</ faq >}}

{{< faq "How to install pi or pacman" >}}
As pi is our primary command, it has been always created since you install the Operating System. In case, your pi error or missing, you can install pi or pacman by pix command, to do so:
```
pix i pi
```
{{</ faq >}}

{{< faq "Is KOOMPI OS is free to use?" >}}
KOOMPI OS  is the `free open-source software`, it is free to use as much as everyone like it. KOOMPI OS is fully customized and self-customizable which make it more special.
{{</ faq >}}

{{< faq "What is pi ?" >}}
The `pi` which is the shortcut formation of `pacman` is one of the majority features of our System. It is a combination of simple binary package manager with the easy-open-source-to-use build system.

If you want to know more details [click here](#).
{{</ faq >}}

{{< faq "What is sudo ?" >}}
**sudo** — A widely used command in the Linux command line, sudo stands for "SuperUser Do". So, if 
you want any command to be done with administrative or root privileges, you can use the sudo 
command.

If you want to know more details [click here](#).
{{</ faq >}}

{{< faq "What is different between pi and pix ?" >}}
As you know that pi is the shortcut form of pacman which we are using it to install applications and 
packages. Even though we had some updates we still using pi as the main command. 

Pix sounds familiar to `pi`, but it is quite different because it stands for **pacman extended or extra** which is supported by many more applications.., etc. that **Pi** can't support like Microsoft office. 
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
For example: In order to install `firefox`,
```
pi -S firefox
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

{{< faq "How can I reset the password of the computer ? " >}}
Dealing with forget password is not an easy thing !!!

KOOMPI respect `user privacy 100%`, so KOOMPI knows nothing about user password or any data. It is the **user's responsibility** to take care of their data and password. However, there is still a way to `set a new password`, but it requires **advanced administration skills**.

Please bring your laptop to the KOOMPI office.
{{</ faq >}}

