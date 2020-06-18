---
title: "System Manager"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
draft: false
# search related keywords
keywords: ["induct", "instate"]
---
**Systemctl** is init system and `system manager` that is widely becoming the new standard for opensource machines. While there are considerable opinions about whether **systemd** is an improvement over the traditional `SysV` init systems it is replacing, the majority of distributions plan to adopt it or have already done so.

Due to its heavy adoption, familiarizing yourself with `systemd` is well worth the trouble, as it will make administering servers considerably easier. Learning about and **utilizing the tools and daemons** that comprise `systemd` will help you better appreciate the power, flexibility, and capabilities it provides, or at least help you to do your job with minimal hassle.

In this guide, we will be discussing the `systemctl` command, which is the central management tool for controlling the init system. We will cover how to manage services, check statuses, change system states, and work with the configuration files.


Please note that although systemd has become the default init system for many Linux distributions, it isn’t implemented universally across all distros. As you go through this tutorial, if your terminal outputs the error bash: systemctl is not installed then it is likely that your machine has a different init system installed.