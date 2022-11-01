---
title: "Change Password in linux"
date: 2022-10-02
categories:
  - Linux
  - Networking
tags:
  - Ubuntu
draft: false
---
## Change the Password by Linux Command Line

First, we will see how a user can change his own password. For that, the passwd command is used followed by the username as shown in the following:
```bash
passwd <username>
```
First, the user is prompted to provide the current password. Once it is accepted, the user gives the new password. 

## Change the Password for Another User

Sudo allows an access as a super user after accepting the password for sudo. After that, you will be prompted to change the password for the mentioned user.
```bash
sudo passwd <username>

```
## Change the Sudo Password

To change the sudo password, you need as a super user. To do that, execute this command and then provide a sudo password:
```bash
sudo -i
```
Once you get the root access after providing the sudo password, execute the passwd command followed by the username to change the password:
```bash
passwd <username>
```
You can also directly use the passwd command with sudo. First, you will be prompted to enter the sudo password. Once accepted, you can change the root password as we did before.
```bash
sudo passwd root
```
This is how we use the Linux command line to change the password. 