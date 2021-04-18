---
layout: page
title: WiFiHacking101
permalink: /Tutorials/TryHackMe/WiFiHacking101/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
<br/><br/>
<br/><br/>
<br/><br/>
Flags will be **BOLD**
<br/><br/>
<br/><br/>
<br/><br/>


**This one does not seem to have a machine to attack**

TASK 1
----

What type of attack on the encryption can you perform on WPA(2) personal?
***Brute Force***

Can this method be used to attack WPA2-EAP handshakes? (Yea/Nay)
***Nay***

What three letter abbreviation is the technical term for the "wifi code/password/passphrase"?
***PSK*** aka Pre-Shared Key

What's the minimum length of a WPA2 Personal password?
***8***


TASK 2
----

How do you put the interface “wlan0” into monitor mode with Aircrack tools? (Full command)

For this the [newbie guide](https://www.aircrack-ng.org/doku.php?id=newbie_guide) tells us we just need to input

***airmon-ng start wlan0*** For myself I need to run

```sudo airmon-ng start wlan0``` But the seems like a semi normal issue 


What is the new interface name likely to be after you enable monitor mode?




What do you do if other processes are currently trying to use that network adapter? 
***airmon-ng check kill*** will check for processes trying to use the adapter

<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
