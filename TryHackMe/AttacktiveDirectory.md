---
layout: page
title: AttacktiveDirectory
permalink: /Tutorials/TryHackMe/AttacktiveDirectory/
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


```nmap -n -sn 10.10.185.0-255```

<img src="/images/TryHackMe/AttacktiveDirectory/IPs.png">

Lets scan them in order and try to figureout the total ports open

```nmap 10.10.185.18```

<img src="/images/TryHackMe/AttacktiveDirectory/IPPorts.png">

After looking at the ports that are open 112 has a domain service on 53 which makes sense for this challenge as well as a kerberos-sec on 88

Task 2
---

We need to use git clone to install Impacket

```sudo git clone https://github.com/SecureAuthCorp/impacket.git /opt/impacket```

Now we need to install the Python requirements

```sudo pip3 install -r /opt/impacket/requirements.txt```

I had all of the requirements installed already but it never hurts to check

Now we can run the Python install script

```cd /opt/impacket/ && python3 ./setup.py install```

That did not work and mentioned a possible permission issue

Since it brought me into the /opt/impacket/ directory I can just use

```sudo python3 ./setup.py install```

Apparently we finally need to install Bloodhound & Neo4j

```sudo apt install bloodhound neo4j```

Task3
---

Question 1 asks what tool can enumerate port 139 & 445

A qucik google search lets me know that the answer is

<img src="/images/TryHackMe/AttacktiveDirectory/Task3-Question1.png">

**Enum4Linux**

Question 2 asks "What is the NetBIOS-Domain Name of the machine?"

Well lets try Enum4Linux

```Enum4Linux 10.10.185.112```

About 30 seconds in I saw a domain name which should be the NetBIOS-Domain Name as well

<img src="/images/TryHackMe/AttacktiveDirectory/DomainName.png">

**THM-AD**

Question 3 asks "What invalid TLD do people commonly use for their Active Directory Domain?"

With having a few hints as to the Top Level Domain (TLD) already and the hint telling us "Spoiler: The full AD domain is spookysec.local" This lets me know that the answer should be

**.local**


Task 4
---

For this task we are given a new program named Kerbrute and a User & Passwordlist to use (mainly to allow faster tutorials)

Lets get it installed!

```sudo pip3 install kerbrute```


I want a directory for these files to keep them organized

```cd /home/kali/ && mkdir THM```

```nano Userlist.txt```

Press CTRL+X
Press Y
Press ENTER

I pasted in the Userlist and I will then do the same with the passwords


For Question 1 I needed to "cheat" the help log showed me nothing of use

<img src="/images/TryHackMe/AttacktiveDirectory/Kerbrute.png">

Apparently the answer was

**userenum**

Question 2 asks "What notable account is discovered? (These should jump out at you)"

After some fumbling I tried this command

```kerbrute -domain spookysec.local -users Userlist.txt```

It seems to have stalled...

One site said to add the IP to my /etc/hosts so lets try that

```nano /etc/hosts```

After adding the IP and a name for it I instantly started finding users so it must be needed


The answer to Question 2 should be svc-admin since that is not a normal name

**svc-admin**


Question 3 asks "What is the other notable account is discovered? (These should jump out at you)"

After waiting I realized something must be wrong when one walkthrough showed the names only taking seconds apart not minutes

```kerbrute -domain spookysec.local -users Userlist.txt -t 100```

the "-t 100 made it go much faster!

**backup**

<img src="/images/TryHackMe/AttacktiveDirectory/KerbruteNames.png">

We made it!

<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
