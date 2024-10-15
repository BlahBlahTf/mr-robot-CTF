<div align="center">
  <h2><b>Hacking Lab - Mr.Robot's CTF</b></h2>
</div>

In this project I will be setting up a hacking lab using Kali Linux and a vulnerable machine from VulnHub.

1) Download VirtualBox, VirtualBox Ext, Kali linux, and mr.robot from vulnHub

2) After importing OVA files, I will now isolate the network by modifying it on VirtualBox. I made sure that on settings both Kali Linux and Mr.robot were both connected to the same internal network.

Insert Pictures*

3) Creating a DHCP server so that the isolated network can get an IP address.

Picture 1 - Changing the Directory to where VirtualBox is installed

Picture 2 - Using VirtualBox to create a DHCP server, in this command line, I have used “vboxmanage dhcpserver” a tool that will help me create a DHCP server,  “add” adding a DHCP server, “—network=WHATEVER THE NAME I CHOSE” to 

4) Open Kali Linux, log in using the default credentials, I am checking to make sure that I got an actual IP address

5) Now I will be checking to make sure that this VM is isolated and that it can’t communicate with anything and my my host laptop can communicate with it.

6) After verifying that they can not communciate with each other I will open up Mr.robot and start hacking

7) I will start this command, sudo map -sS -T4 10.38.1.110-120

Insert Picture

8) After using nmap, I was able to see the ports and notice that there are 22, 80, and 443 which tells me that this is probably a webserver, I open Firefox and type in the ip address given on the nmap.

9) There are 3 flags I willl try to find.
