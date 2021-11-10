# Hacky Pi Handout :robot:
This repository contains context information to the security challenges created in https://github.com/nimarty/hackypi/.

## Challenges
- [chatty-charly](chatty-charly/chatty-charly.md)
- [relaxed-rachel](relaxed-rachel/relaxed-rachel.md)

## General Setup
You get a Raspberry Pi together with a prepared SD card for this training. A minimal image is provided that enables to install challenge packages from a OPKG server. To do so, connect the Raspberry Pi to a network with a DHCP server or directly to your computer. For the second option, you temporarely need access to the UART interface in order to set a static IP address in the file `/etc/dhcpcd.conf` by adding those two lines in the end:
```
interface eth0
static ip_address=192.168.1.12/24
```
Remove the UART interface afterwards and try to solve the challenges **only** over the network connection. Do always remove the challenge's package as mentioned in each cleanup section in the documentation. You should never have two challenges installed simultaneously.

## Contribute
For each security challenge there should be a folder with the same name in this repository, e.g. chatty-charly, or relaxed-rachel.
If a challenge requires some precompiled binaries to run under Linux, they should be placed together with documentation in the subdirectory.
