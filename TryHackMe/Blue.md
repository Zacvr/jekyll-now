---
layout: page
title: Blue
permalink: /Tutorials/TryHackMe/Blue/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
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
"nap --script vuln -p 135-445 10.10.161.31 -v"
<br/><br/>
"--script vuln" will load in scripts to scan on the target IP/Ports
<br/>
"-p 135-445" will scan ports 135-445 with those vulnerability script
<br/>
"-v" increases the verbosity *adds more words* (you can use -vv for a greater effect)
<br/><br/>

<br/><br/>
Now we have our final flag of task 1!
<br/><br/>
in our command we see "ms17-010" it even shows the disclosure date right below the red box
<br/><br/>
<br/><br/>
<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
