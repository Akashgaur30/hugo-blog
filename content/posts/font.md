---
title: "How to add Font"

date: 2022-11-13
url: /font/
categories:
  - Linux
  - Windows
  - Networking
tags:
  - Ubuntu
draft: false
---
# How to add font in arch linux
![font](/image/2.png "font")

## first download font add in this directories

As you can see, directories that are scanned for font files are declared using the <dir> tag. The following directories are set by default:
```bash
cd /usr/share/fonts
```
## Generating and updating the fonts cache

To make the directories where fonts are stored re-scanned, and the font cache be re-created (typically we want to do this after we install a new font), we can use the fc-cache utility. If invoked without any argument, the utility re-scans all configured directories:
 ```
 fc-cache
 ```
 If we want to get information only about a specific font pattern, we can pass it as argument to the command
 ```
 fc-list 
 ```
 ## My favourite font 
 monaca
 
 
 
 ## For console font
 
 If you use the Linux console, the best way I found is:
 ```
 /etc/default/console-setup
 ```
 put, for example

```
CHARMAP="UTF-8"
CODESET="Lat7"
FONTFACE="Terminus"
FONTSIZE="28x14"

```
##Another
way is to use setfont from the kbd package:
```
setfont /usr/share/consolefonts/Lat7-Terminus28x14.psf
```
