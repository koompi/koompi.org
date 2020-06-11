---
title: "Social Media Apps"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: true
# search related keywords
keywords: ["induct", "instate"]
---
## Discord
**Discord** is a proprietary freeware VoIP application and digital distribution platform designed for
video gaming communities, that specializes in text, image, video and audio communication between
users in a chat channel
In order to install this app you have to run it on terminal and typing this:
```
 pi -S discord
```
## Kodi
**Kodi** is one of the best free and open source media server software available in the market. It offers
an intuitive graphical user interface with lots of customization options. Kodi is an all in one
entertainment software center which supports all the primary OS including Android.
```Text
 pi -S kodi
```
## Popcorn Time
**Popcorn Time** is a multi-platform, free software BitTorrent client that includes an integrated media
player. Popcorn Time provide a free "alternative" to subscription-based video streaming services such as
Netflix.
```Text
pi -S popcorntime-bin
```
or you can run this other one:
```
pi -S popcorntime
```
## Teamviewer
**Team Viewer** is an awesome application for remotely accessing a computer or letting someone
remotely access your computer. It is easy to use and its completely free of charge.
To install it using this command:
```Text
pi -S teamviewer
```
In order to restart your teamviewer, you can simply run this command:
```
sudo systemctl enable teamviewerd
```
You can start your teamviewer service with command line also:
```
sudo systemctl start teamviewerd
```
## Dingtalk
**Dingtalk** is an enterprise communication and collaboration platform developed by Alibaba Group. It
was one of the world's largest professional communication and management mobile apps in China with
over 100 million users.
Dingtalk can be installed by command below:
```
pi -S dingtalk
```
## Messenger
**Messenger** is a messaging app and platform developed by Facebook, Inc.The Users can send
messages and exchange photos, videos, stickers, audio, and files, as well as react to other users'
messages and interact with bots. The service also supports voice and video calling. The standalone apps
support using multiple accounts, conversations with optional end-to-end encryption, and playing games
through this app.
You can install messenger by run this command:
```
 pi -S caprine
```
## Skype
**Skype** is a telecommunications application that specializes in providing video chat and voice calls
between computers, tablets, mobile devices, the Xbox One console, and smartwatches via the Internet.
Skype also provides instant messaging services. Users may transmit text, video, audio and images.
You can install app by the following steps below:
##### Step 1: Update Your System
In order to update your system run this:
```
 pi -Syy
```
## Zoom Video
[Zoom](https://zoom.us/) is a web-based video conferencing tool with a local, desktop client and a
mobile app that allows users to meet online, with or without video. Zoom users can choose to record
sessions, collaborate on projects, and share or annotate on one another's screens, all with one easy-touse platform.
You can install zoom by run the command below:
```
pi -i zoom
```
or
```
pi -S zoom
```
If you are facing error of installing zooom please run thic command below or [Click
here](https://koompi.org/Common-Problems#my-zoom-isnt-running-even-i-reinstalled-it-the-way-tosovle-it-is):
```
pi -S --noconfirm zoom
```
## Telegram
**Telegram** is a cloud-based cross-platform instant messaging service with optional end-to-end
encryption. Account creation requires a phone number.
The official clients are open-source but the code for recent versions is not always immediately
published. The server-side code is proprietary.
You can use one of following methods in order to use Telegram:
>
> **Tips:** We are recommending these two commands for installing:
{.is-success}
```
pi -S telegram-desktop`, built by Arch Linux
```
The other one
```
pi -S telegram-desktop-bin`, built by upstream
```
## Wechat
**WeChat** is more than a messaging and social media app – it is a lifestyle for over one billion users
across the world. It is free and safe downloaded.
You can install it on our OS by 2 ways.
**The first way:**
Open terminal and run this command:
````
pi -S electronic-wechat-bin`
````
> **Tips:** We recommended you to use **the second way**.It is easier and not much question.
{.is-success}
**The Second way:**
```
curl -S http://repo.koompi.org/packages/electronic-wechat-bin-2.3.1-1-x86_64.pkg.tar.xz -O && sudo
pacman -U electronic-wechat-bin-2.3.1-1-x86_64.pkg.tar.xz && sudo pacman -S nss gtk3 libxss
```
