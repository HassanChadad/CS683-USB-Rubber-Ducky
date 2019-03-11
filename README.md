# Offensive Security and the USB Rubber Ducky
## Hassan Chadad
## CS-683 USB Rubber Ducky Assignment

**Research the scripts and tools available for the "USB Rubber Ducky". <br/> Read Part II of: 2011 - Gray Hat Hacking.pdf <br/> Document in 'mark-down' a crib-sheet of exact steps and all tools required to for two or more different exploits of a host platform. Update the scripts or find other tools as necessary for a complete attack.**

To understand more what ducky script is, I read this link https://www.hak5.org/gear/duck/writing-your-first-usb-rubber-ducky-payload
<br/><br/>
A ducky script can be written in any standard ASCII text editor (gedit, nano, vi, emacs, vim, or even notepad).<br/>
The ducky scripts that interested me were targeting Windows OS because I am a Windows user.<br/><br/>

The link below has a good collection of USB Rubber Ducky Scripts
https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payloads

The most interesting ducky scripts from the above link were:
* [Fork-Bomb](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payload---fork-bomb)
    * The developer create a batch script inside the Startup Folder that goes in an infinite loop starting itself over and over. The batch script will basically run on startup and cause the PC to shutdown from the infinite processes being created.
* [Wifi-Grabber](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payload---WiFi-key-grabber)
    * The developer runs the cmd in admin mode and creates a new Directory "l", then exports all the wifi passwords to it and send all the xml files to SFTP.

I updated some scripts to do different attacks:
* [Chrome History Stealer](https://github.com/HassanChadad/CS683-USB-Rubber-Ducky/blob/master/Chrome-History-Stealer.md)
* [Spyware Launcher](https://github.com/HassanChadad/CS683-USB-Rubber-Ducky/blob/master/spyware_launcher.md)
* [Infinite Shutdowns](https://github.com/HassanChadad/CS683-USB-Rubber-Ducky/blob/master/Infinite_shutdowns.md)





