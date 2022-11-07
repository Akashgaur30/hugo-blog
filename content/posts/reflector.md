---
title: "How to install reflector"
date: 2022-10-03
url: /reflector/
categories:
  - Linux
tags:
  - Ubuntu
  - Arch linux
draft: false
---
#Reflector


Reflector is a small Python3 script that sort through the Arch Linux mirrors based on parameters of your choice and updates your mirrorlist.

**_More info:_** [Reflector - ArchWiki](https://wiki.archlinux.org/index.php/Reflector) | [Project website - xyne](https://xyne.archlinux.ca/projects/reflector/)

## Installation
```bash
pacman -S reflector
```

## Usage

`reflector --help` will show you the available commands and their options.

The following command will update your mirrorlist with the 50 fastest mirrors that have support for both HTTPS and IPV6.

```bash
reflector --verbose --completion-percent 100 --ipv6 --protocol https --score 50 --sort rate --save
 /etc/pacman.d/mirrorlist
```

## Service
Reflector can run automatically in the background at chosen intervalls. The default timer will run reflector once a week.

If you want the options from the example earlier make the following changes.

/etc/xdg/reflector/reflector.conf

```bash
--save /etc/pacman.d/mirrorlist
--completion-percent 100
--protocol https
--ipv6
--score 50
--sort rate
```

```bash
systemctl enable reflector.timersy
stemctl start reflector.timer
systemctl start reflector.service
```