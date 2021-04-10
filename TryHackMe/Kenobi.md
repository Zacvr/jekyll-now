---
layout: page
title: Intro To x86-64
permalink: /Tutorials/TryHackMe/IntroTox86-64/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
<br/><br/>
<br/><br/>
<br/><br/>
Flags will be **BOLD**
<br/><br/>
<br/><br/>
<br/><br/>

First lets find the IP in the subnet!


```nmap -n -sn 10.10.113.0-255```

<img src="/images/TryHackMe/IntroTox86/IP.PNG">

"nmap -Pn -F 10.10.113.48,114,123,183,226"

<img src="/images/TryHackMe/IntroTox86/IP Results.PNG">

Now lets try to login with our ssh creds on ach IP since they all have SSH

"ssh tryhackme@10.10.113.114"

"reismyfavl33t"



<img src="/images/TryHackMe/IntroTox86/Task 7.PNG">


<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
