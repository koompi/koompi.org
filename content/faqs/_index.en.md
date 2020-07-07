---
title: "FAQs"
draft: false
date: 2018-12-26T11:02:05+06:00
icon: "ti-help-alt"
description: "Solutions and Problems that happened in the Operating System have been noted here."
type : "docs"
---
{{< faq "How to install KOOMPI OS?" >}}
There are two main steps for installing it.

**First Step (Create a bootable USB)**
- Get a USB minimum of 4GB.
- Install the Etcher.
- Download the OS source through this [link](https://repo.koompi.org/iso/KOOMPI-OS-2020.04.26-x86_64.iso).
- Move those source into the USB and start making it a bootable drive.
**Second Step (Setup OS into the PC)**
- Plug the USB  to your PC.
- Open the PC and Move into the BIOS Boot(When you opened press key `Esc`.).
- Go to Booting Menu.
- After that Select the USB.
- After that you will run some process and when it finished, your screen is going to show Desktop.
- Connect to the Internet and Click on App that uses for installing and follow the instructions have been given.

For making it easier, click this [link for the video](https://youtu.be/DnavvK4NU6A).
{{</ faq >}}

{{< faq "How to install pi or pacman" >}}
As pi is our primary command, it has been always created since you install the Operating System. In case, your pi error or missing, you can install pi or pacman by pix command, to do so:
```
pix i pi
```
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
As you know Spotify is not available in some countries !!
{{< /notice >}}
{{</ faq >}}

{{< faq "Can KOOMPI OS run with IOS ?" >}}
In the meantime, our software isn't supporting the IOS system yet, but we are looking forward to doing it.
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
Not exactly, You can download it by it is not running smoothly. To install it, you need to instal `pix` first, [Click here](https://www.koompi.org/release/pix-release/pix_release/).
{{</ faq >}}


{{< faq "When will a new version of KOOMPI OS release?" >}}
All Announcement about releasing the new version of KOOMPI OS will be announced in [KOOMPI Telegram Community](https://t.me/koompi). And it will be informed on the new release section on the www.koompi.org](https://www.koompi.org/release/) as well.
{{</ faq >}}

{{< faq "How to update the system in KOOMPI OS?" >}}
In KOOMPI OS, You can update the system by using the Konsole or command-line tools and a command like this.  
```
pi -Sy
```
{{</ faq >}}

{{< faq "Applications can not run, How to solve it ?" >}}
As your apps can not run, you might be facing error related to missing dependencies of the apps. To know, what kind of dependencies that your apps required. You need to run the keyword of the package name, and it  will show your missing dependencies.[Visit here to see all the dependencies](#).

Sample: I am facing with can not run **telegram app**. So, the keyword packages of telegram app is `telegram-desktop`. I run the keyword in Konsole:
```
telegram-desktop
```
The output will be showing and you can see the name of dependencies that are missing, mostly all apps are missing QT5, libicu. We can install dependency packages back by  run:
```
pi -S <Name of dependency packages>
```
{{</ faq >}}



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
In general, After you have installed the OS each of the apps will choose their default app which has been decided by developer but you can change it with the following steps:
1. you need to search for `System setting`.
1. After that, you have to find the `Applications` section.
1. Then, you will find the `Default Applications` layout.
1. Finally, Selecting the program you want it to change and applying it.

Sample: As my web browser has been using elinks as my default app, so I want to change it and using firefox instead. I follow the following step and in the `Default Applications` section. I look for web browser and apply firefox instead of elinks. That's done. now I have used Firefox as my default browser.
{{</ faq >}}

{{< faq "Is KOOMPI OS is free to use?" >}}
KOOMPI OS  is the `free open-source software`, it is free to use as much as everyone like it. KOOMPI OS is fully customized and self-customizable which make it more special.
{{</ faq >}}

{{< faq "What is pi ?" >}}
The `pi` which is the shortcut formation of `pacman` is one of the majority features of our System. It is a combination of simple binary package manager with the easy-open-source-to-use build system.

If you want to know more details [click here](#).
{{</ faq >}}

{{< faq "What is sudo ?" >}}
**sudo** — A widely used command in the Linux command line, sudo stands for "SuperUser Do". So, if you want any command to be done with administrative or root privileges, you can use the sudo command.

If you want to know more details [click here](#).
{{</ faq >}}

{{< faq "What is different between pi and pix ?" >}}
As you know that pi is the shortcut form of pacman which we are using it to install applications and packages. Even though we had some updates we still using pi as the main command. 

Pix sounds familiar to `pi`, but it is quite different because it stands for **pacman extended or extra** which is supported by many more applications.., etc. that **Pi** can't support like Microsoft office. 
{{</ faq >}}

{{< faq "How to install pi or pacman?" >}}
you can install pi or pacman by pix command, to do so 
```
pix i pi
```
{{</ faq >}}
{{< faq "How to setup keyboad, font and more?" >}}
There are different ways to install each feature, please [visit this for guide-line and details](#).
{{</ faq >}}


{{< faq "I can't update my computer and it is requiring keys!" >}}
It means you are no longer sync with OS Repo or your repo has been corrupted or invalided. You can 
solve the problems by running three commands below:

```
sudo pacman -Scc
sudo pacman-key --refresh-keys
sudo pacman -Syyu
```
{{</ faq >}}
{{< faq "What is terminal or konsole ?" >}}
Originally, a konsole was a terminal “plugged into” the computer: it provided the interface that was 
used to configure and control the computer and to view messages from the operating system.

When a Linux server first boots, it prints status messages to the console, the familiar scroll of text that brings joy to many a Linux user. When you interact with your server, you connect a terminal to a program running in a console.
{{</ faq >}}

{{< faq "How to install applications in KOOMPI OS ?" >}}
To install the application in KOOMPI OS, you have to use commands in terminal or Konsole:
**Sample:**
```
 pi -S Package_Name
```
For example: To install `firefox`,
```
pi -S firefox
```
Please, click [here](https://www.koompi.org/applications/) for more info.
{{</ faq >}}



{{< faq "How to Change password in KOOMPI OS ?" >}}
As a KOOMPI OS or Linux system administrator (sysadmin), you can change the password for any users on your server. To change a password on behalf of a user:

1. First, sign on or “`su`” or “`sudo`” to the “`root`” account on **Pionux**, run: `sudo -i`
1. Then type, `passwd Administrator_name` to change a password for Admin user
1. The system will prompt you to enter a password twice.


For more info about password: [Click here]()
{{</ faq >}}

{{< faq "How can I reset the password of the computer? " >}}
Dealing with forget password is not an easy thing !!!

KOOMPI respect `user privacy 100%`, so KOOMPI knows nothing about user password or any data. It is the **user's responsibility** to take care of their data and password. However, there is still a way to `set a new password`, but it requires **advanced administration skills**.

Please bring your laptop to the KOOMPI office.
{{</ faq >}}

{{< faq "How can I change screen resolution? " >}}
You can change the screen resolution by going into `System Setting` and then `Hardware` and then move on to `Display and Monitor` section. After that **Click** `Display Configuration`.

The default resolution for most PCs is **1920x1080** so does KOOMPI. So, set it to that resolution.
{{</ faq >}}

{{< faq "Sound problem, What should I do? " >}}
There are two solutions we are recommending for you.

---
If you are surely having sound problems, Please, Following these instructions:
- Open your terminal and run this command for killing your audio.
```
pulseaudio -k
```
- After that run another command below to make your audio work again. 
```
pulseaudio --start
```
---
If the first solution isn't working you can try with `pavucontroll` which is the app that supporting the audio 
configuration.

To install it run this command below:
```
pi -S pavucontrol
```
After you have installed it, you can search and open it for configuring the input and output audio.

If you try every one of the solutions have been provided and still have problems, please it to our office for fixing.
{{</ faq >}}

{{< faq "My internet is not working, How to fix it? " >}}
We suggest you to reset the **network manager** with the commands below.
```
sudo systemctl restart NetworkManager
```
If it still has the problem, we recommend you to bring it to our office.
{{</ faq >}}

 
{{< faq "How can I know about my pc specs?" >}}
You need to do is that you have to open **Settings** `-->`**System Setting** `-->` **System Information**. Finally, now you can see all details about your pc.
{{</ faq >}}

{{< faq "I can't remove the note from my desktop?" >}}
you need to do is that you need to hold the right click of your mouse on the note. And then the 
remove icon will pop up. That's all.

For more details is that when some app or icon pops up just follow the previous solution.
{{</ faq >}}

{{< faq "How to enable the touchpad while it was off?" >}}
You can open your touchpad through your keyboard. First, you need to go into the **setting** Enter
and Click **System Settings**. And then you will have to find **Input Devices**, Select 
**Touchpad** feature, and then `Enable it` and you will be done.

{{< notice note >}}
Use `tab key` for changing you are selected. If you are finding it hard to do with the keyboard, we recommend using the external mouse instead.
{{< /notice >}}
{{</ faq >}}