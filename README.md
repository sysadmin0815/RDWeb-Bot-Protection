# RDWeb-Bot-Protection
Protect your Windows RDWeb Server from malicious bots and brute force attempts.

## Disclaimer
All information and code is provided as is without any warranty!!<br>
**Always backup** your files before doing changes. Prefered, test the changes in a dev environment first.<br>
The code was **successfully tested on Windows Server 2019** with RDWeb and IIS Role installed.<br>

> [!CAUTION]
> Do not replace the files on your server with copy & paste! This repo contains code snippets only. Modify the files on your server.


## How to implement
Root directory is C:\Windows\Web\
You have to add/replace some code in the files *login.aspx, logoff.aspx* and *webscripts-domain.js*<br><br>
**File locations:**<br>
RDWeb/Pages/webscripts-domain.js<br>
RDWeb/Pages/en-US/login.aspx<br>
RDWeb/Pages/en-US/logoff.aspx<br><br>
*All files in the repo have the .txt name extension. Remove .txt to get the default file name extension*

## Why do I need this code?
I was searching for a "bot protection" for our RDWeb Servers. We tried it with JS and Powershell but was not appy with the results.
Our RDWeb Server got more and more hammered with POST requests, so we had to implement something.<br><br>

**Here is a log (IP addresses removed) before the code was implemented:**<br>
*If your IIS webserver log looks like this, you need it* :) <br>
![image](https://github.com/sysadmin0815/RDWeb-Bot-Protection/assets/81157346/b4c42f42-abad-46f3-90cc-eb6bf85eabb5)
<br>IIS Log default path: C:\inetpub\logs\LogFiles\W3SVC1\xxx.log<br><br>
> [!IMPORTANT]
> The code in this repo works for the webserver only, not the gateway service!
<br>


After the code is implemented the log looks much better.

## How to verify that the code is working?
Check your current webserver logs at *C:\inetpub\logs\LogFiles\W3SVC1* and compaire them with the old logs.

## Credits
Special thanks to [thomas-417](https://github.com/thomas-417) for doing the C#!



