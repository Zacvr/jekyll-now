---
layout: page
title: Kenobi
permalink: /Tutorials/TryHackMe/Kenobi/
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


```nmap -n -sn 10.10.130.0-255```

<img src="/images/TryHackMe/Kenobi/IPs.PNG">

Lets scan them in order and try to figureout the total ports open

```nmap 10.10.130.11```

<img src="/images/TryHackMe/Kenobi/IPPorts.PNG">

**7** is the answer to the first question!

TASK 2
----

It now tells us to run a script for nmap to enumerate shares

```nmap -p 445 --script=smb-enum-shares.nse,smb-enum-users.nse 10.10.130.11```

<img src="/images/TryHackMe/Kenobi/Enum_Shares.PNG">

**3** Shares is the first answer in task 2

lets follow their lesson

```smbclient //10.10.130.11/anonymous```

```Press "Enter"```

We are now inside

we need to view the files now

```ls```

<img src="/images/TryHackMe/Kenobi/Files.PNG">

**log.txt** is the answer to the second question!

we are making great progress lets keep going

```smbget -R smb://10.10.130.11/anonymous```

```press "Enter"```

<img src="/images/TryHackMe/Kenobi/Download.PNG">

We now have a file! Why don't we open it?

```cat log.txt```

Lets look for that FTP port shall we

<img src="/images/TryHackMe/Kenobi/FTP.PNG">

**21** is the FTP port according to the top of this document

This tutorial has another script to run

```nmap -p 111 --script=nfs-ls,nfs-statfs,nfs-showmount 10.10.130.11```

<img src="/images/TryHackMe/Kenobi/Var.PNG">

**/var** is the final answer in task 2!

Task 3
----

We are told to to find the version of ProFtpd the machine is running on the FTP port

```netcat 10.10.130.11 21```

<img src="/images/TryHackMe/Kenobi/ProFtpd.PNG">

**1.3.5** is our first answer in task 3

We now need to findout how many exploits are there for ProFtpd that is running

```msfconsole```

```search ProFtpd```

<img src="/images/TryHackMe/Kenobi/Checking.PNG">

**3** we see 3 with check as "Yes" possibly this is why 3 is correct?

Now lets continue along

```sudo mkdir /mnt/kenobiNFS```

```sudo mount 10.10.130.11:/var /mnt/kenobiNFS```

```ls -la /mnt/kenobiNFS```

Now in theory we should have a network mount that we can find the key for the login












<img src="/images/TryHackMe/Kenobi/Task 7.PNG">


<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
