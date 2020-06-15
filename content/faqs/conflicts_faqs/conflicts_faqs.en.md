---
title: "Conflicted FAQs"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---
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
It appears that I have problem with `modprobe vboxdrv`.You can sovle this problem by run command below:
```
sudo modprobe -a vboxdrv
```
{{</ faq >}}

{{< faq " Invalid or corrupted packages !!!" >}}
First, Run this other command for clearing cache and the database directory
```
pi -Scc
```
After that, run this comman to reinstalling the database and resync repo:
```
pi -Syyu
```
{{</ faq >}}

{{< faq "Facing error with connecting libalpm !!!" >}}
If you facing this probelm run commands below:
**For libalpm:so.11:**
```
sudo ln -s /usr/lib/libalpm.so.10 /usr/lib/libalpm.so.11
```
**For libalpm:so.12:**
```
sudo ln -s /usr/lib/libalpm.so.12 /usr/lib/libalpm.so.11
```
After you finish with tthe command above, you may face other problem realated to `pi error while loading...`. You need to install pi back [click here](https://www.koompi.org/faqs/#how-to-install-pi-or-pacman)
{{</ faq >}}

{{< faq "Facing Xorgprotol issues !!" >}}
As the Xorgprotol issues is not an easy problem. First, we need to remove it and upgrade the system
```
pi -Rdd xorgproto
```
{{< notice info >}}
DO NOT worry, `Xorgprotol package` is safe for removing. 
{{< /notice >}}

Despite this thread being `[SOLVED]`, Facing nonethless with notified status.
```
removing xorgproto breaks dependency 'xorgproto' required by xorg-server-devel
```
in this case, the `xorgproto packages` has been used by xorg-server-devel packages, we can remove the packages and start remove **xorgprotol again.**
```
pi -Rdd xorg-server-devel
```
{{</ faq >}}


{{< faq "Missing Qt5 dependency, How to install it back ? " >}}
If you accidentally delete QT5 dependency or while you are trying to install some app and it required the Qt5 pacckages, you can install it back by:
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

{{< faq "Facing errors with mirrors out of date !! " >}}
Nothing to worry, as it is out of date not out of sync, we can solve it with only command:
```
sudo pacman-mirrors -f 5
```
After, it has done running, try to update with command `pii -Syyu`.
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

{{< faq "Conflicted with python-pygmets, How to fix it ?" >}}
In order to solve this conflicted, you need to remove the existing packages in the file system by running this command below:
```
sudo rm -rf /usr/bin/pygmentize
```
After that try to update your system with command:
```
pi -Syu
```
{{< notice info >}}
All the commands must run in **Konsole**.
{{< /notice >}}
{{</ faq >}}