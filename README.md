# Hacky Pi Handout :robot:
This repository contains context information to the security challenges created in https://github.com/nimarty/hackypi/.

## Challenges
- [chatty-charly](chatty-charly/chatty-charly.md)
- [relaxed-rachel](relaxed-rachel/relaxed-rachel.md)
- [deceived-donald](deceived-donald/deceived-donald.md)
- [moody-maggie](moody-maggie/moody-maggie.md)
- [tearful-tanja](tearful-tanja/tearful-tanja.md)
- [raging-rachel](raging-rachel/raging-rachel.md)
- [hefty-howard](hefty-howard/hefty-howard.md)

## General Setup
You get a Raspberry Pi together with a prepared SD card for this training. A minimal image is provided that enables to install challenge packages from a OPKG server. To do so, connect the Raspberry Pi to a network with a DHCP server or directly to your computer. For the second option, you temporarely need access to the UART interface in order to set a static IP address in the file `/etc/dhcpcd.conf` by adding those two lines in the end:
```
interface eth0
static ip_address=192.168.1.12/24
```
Remove the UART interface afterwards and try to solve the challenges **only** over the network connection. Do always remove the challenge's package as mentioned in each cleanup section in the documentation. You should never have two challenges installed simultaneously.

## Setup with Windows
Here is some additional information if your host computer is running Windows:
- Your computer is connected to the internet with an ethernet cable and the Raspberry Pi is connected directly to your computer with an ethernet cable too. The profile of the direct connection should be set to private to avoid having to set special firewall rules. So open a PowerShell with admin rights, get the index of the profile and set it to private:  
&rarr; ``Get-NetConnectionProfile``  
&rarr; ``Set-NetConnectionProfile -InterfaceIndex \<Index\> -NetworkCategory Private``  
If you cannot connect, add a rule to your firewall to allow access to your Raspberry Pi:  
&rarr; Go to *Windows Defender Firewall* --> *Advanced settings* --> *Inbound Rules*  
&rarr; Create a new rule to allow access from the Raspberry Pi's IP address  
- If your computer is connected via WiFi, it is very difficult to establish a direct connection with an Ethernet cable. Therefore, the Raspberry Pi should be connected to the same network as your computer and get the IP that the Raspberry Pi got. Maybe you can also set the IP address as static in the DHCP server of your network (if it is your private one).


## Contribute
For each security challenge there should be a folder with the same name in this repository, e.g. chatty-charly, or relaxed-rachel.
If a challenge requires some precompiled binaries to run under Linux, they should be placed together with documentation in the subdirectory.
