---
title: "Frequently Asked Questions"
draft: false
---
----
----
### General FAQs
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

{{< faq "How to install pi or pacman?" >}}
As pi is our primary command, it has been always created since you install the Operating System. In case, your pi error or missing, you can install pi or pacman by pix command, to do so:
```
pix i pi
```
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

{{< faq "Can KOOMPI OS be able to install Spotify ?" >}}
Of Course, you can install it. [Visiting here to know how to install applications in KOOMPI OS](https://www.koompi.org/applications/).
{{< notice note >}}
As you know Spotify is not available in some countries !!
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
Not exactly, You can download it by it is not running smoothly. To install it, you need to instal `pix` first, [Click here](https://www.koompi.org/release/pix-release/pix_release/).
{{</ faq >}}


{{< faq "When will a new version of KOOMPI OS release?" >}}
All Announcement about releasing the new version of KOOMPI OS will be announced in [KOOMPI Telegram Community](https://t.me/koompi). And it will be informed on the new release section on the www.koompi.org](https://www.koompi.org/release/) as well.
{{</ faq >}}

{{< faq "What is terminal or konsole ?" >}}
Originally, a konsole was a terminal “plugged into” the computer: it provided the interface that was 
used to configure and control the computer and to view messages from the operating system.

When a Linux server first boots, it prints status messages to the console, the familiar scroll of text that brings joy to many a Linux user. When you interact with your server, you connect a terminal to a program running in a console.
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

{{< faq "How to update the system in KOOMPI OS?" >}}
In KOOMPI OS, You can update the system by using the Konsole or command-line tools and a command like this.  
```
pi -Sy
```
{{</ faq >}}

{{< faq " How can I change default apps has been used ?" >}}
In general, After you have installed the OS each of the apps will choose their default app which has been decided by developer but you can change it with the following steps:
1. you need to search for `System setting`.
1. After that, you have to find the `Applications` section.
1. Then, you will find the `Default Applications` layout.
1. Finally, Selecting the program you want it to change and applying it.

Sample: As my web browser has been using elinks as my default app, so I want to change it and using firefox instead. I follow the following step and in the `Default Applications` section. I look for web browser and apply firefox instead of elinks. That's done. now I have used Firefox as my default browser.
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

{{< faq "Disable/Able auto start for application!" >}}
you can disable or able it by go to system setting-> Startup and shutdown -> auto start and disable the app you don't want it to start automatically when you open your pc.
{{</ faq >}}


### Technical Issue FAQs
{{< faq "Cannot connect to the  wifi and have anbox installed!" >}}
Opening Konsole and run the commands below
```
pi -R linux-lts

sudo grub-mkconfig -o /boot/grub/grub.cfg 

reboot
```
After rebooting, you should be able to connect the wifi. Then you have to open konsole
```
pix i e11-firmware
```
{{</ faq >}}

{{< faq "Notes, widget, panel issues!" >}}
There is a known bug happened to some of us where the desktop widgets or panels keep reappearing after removed. This now can be solved easily by installing Refresher from our Pix. The commands below demonstrate how you can solve this problem.

1. Installing Refresher
```
pix install refresher
```
2. Using Refresher
```
refresher panel
```
To fix the panel problem
```
refresher widget 
```
To fix the widgets problem
```
refresher all
```
To fix both panels and widget
{{</ faq >}}

{{< faq "Missing  firmware, cannot connect to wifi!" >}}
If  you can use Bluetooth tether through USB, then open terminal; type: 
```
pix -i e11-firmware 
```
The latest e11 installers work out of the box. 
{{</ faq >}}

{{< faq "When I open the pc, it shows only back screen like below!!!" >}}
```
Loading Linux linux...
error: premature end of file /boot/vmkinuz-linux
Loading initial ramdisk ...
error: you need to load the kernel first,

Press any keys to continue...._
```
Your kernel is corrupted. This happens due various reasons such as:
- improper shutdown
- incomplete update

Please bring to [KOOMPI Office](http://bit.do/koompi-boran), we will fix for you.
{{</ faq >}}

{{< faq "Zoom issue and can not run !!!" >}}
As the `ZOOM` is requiring the `QT5`, you can run the command below:
```
pi -S --noconfirm xz qt5-webengine zoom
```
After, Finish the command and zoom still not running, [Click here](#).
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

{{< faq "I can't update my computer and it is requiring keys!" >}}
It means you are no longer sync with OS Repo or your repo has been corrupted or invalided. You can 
solve the problems by running three commands below:

```
sudo pacman -Scc
sudo pacman-key --refresh-keys
sudo pacman -Syyu
```
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


{{< faq "Conflicting with  p11-kit-trust ?" >}}
Meanwhile, you are updating the OS and you are facing this kind of conflicting.

Sample of output you are commonly facing:
```
problem: nss: /usr/lib/p11-kit-trust.so exists in filesystem
lib32-nss: /usr/lib32/p11-kit-trust.so exists in filesystem
```
As you can notice that `p11-kit-trust.so`, you need to overwrite it.
```
sudo pacman -Syu --overwrite /usr/lib\*/p11-kit-trust.so
```
{{</ faq >}}

{{< faq "Error with Modprobe and Vboxdrv ?" >}}
It appears that I have a problem with `modprobe vboxdrv`.You can solve this problem by run command below:
```
sudo modprobe -a vboxdrv
```
{{</ faq >}}

{{< faq " Invalid or corrupted packages !!!" >}}
First, Run this other command for clearing cache and the database directory
```
pi -Scc
```
After that, run this command to reinstalling the database and resync repo:
```
pi -Syyu
```
{{</ faq >}}

{{< faq "Facing error with connecting libalpm !!!" >}}
If you facing this problem run commands below:
**For libalpm:so.11:**
```
sudo ln -s /usr/lib/libalpm.so.10 /usr/lib/libalpm.so.11
```
**For libalpm:so.12:**
```
sudo ln -s /usr/lib/libalpm.so.12 /usr/lib/libalpm.so.11
```
After you finish with the command above, you may face other problem related to `pi error while loading...`. You need to install pi back [click here](https://www.koompi.org/faqs/#how-to-install-pi-or-pacman)
{{</ faq >}}

{{< faq "Facing Xorgprotol issues !!" >}}
As the Xorgprotol issues is not an easy problem. First, we need to remove it and upgrade the system
```
pi -Rdd xorgproto
```
{{< notice info >}}
DO NOT worry, `Xorgprotol package` is safe for removing. 
{{< /notice >}}

Despite this thread being `[SOLVED]`, Facing nonetheless with notified status.
```
removing xorgproto breaks dependency 'xorgproto' required by xorg-server-devel
```
in this case, the `xorgproto packages` has been used by xorg-server-devel packages, we can remove the packages and start remove **xorgprotol again.**
```
pi -Rdd xorg-server-devel
```
{{</ faq >}}


{{< faq "Missing Qt5 dependency, How to install it back? " >}}
If you accidentally delete QT5 dependency or while you are trying to install some app and it required the Qt5 packages, you can install it back by:
```
pi -S qt5-base
```
{{</ faq >}}
{{< faq "How to refresh the importing of Key? " >}}
In order to refreshing your PGP Key on KOOMPI OS, you need to run these following lines in Konsole:
```
sudo pacman -Scc
sudo pacman-key --refresh-keys
sudo pacman -Syyu
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

{{< faq "Facing errors with mirrors out of date !! " >}}
Nothing to worry, as it is out of date not out of sync, we can solve it with only command:
```
sudo pacman-mirrors -f 5
```
After, it has done running, try to update with command `pi -Syyu`.
{{</ faq >}}

{{< faq "Conflicting python-pyqt5 and pyqt5-common, How to fix it ?" >}}
If you run command to update the system and facing error like below:
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
To solve this problem, you have to run this command and follow all instructions have been given.
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

{{< faq "Conflicted with python-pygmets, How to fix it ?" >}}
To solve this conflict, you need to remove the existing packages in the file system by running this command below:
```
sudo rm -rf /usr/bin/pygmentize
```
After that try to update your system with the command:
```
pi -Syu
```
{{< notice info >}}
All the commands must run in **Konsole**.
{{< /notice >}}
{{</ faq >}}