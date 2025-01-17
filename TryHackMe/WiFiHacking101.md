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
***wlan0mon*** Since it is in monitoring mode it will add the mon


What do you do if other processes are currently trying to use that network adapter? 
***airmon-ng check kill*** will check for processes trying to use the adapter


What tool from the aircrack-ng suite is used to create a capture?
***airodump-ng***


What flag do you use to set the BSSID to monitor?

<img src="/images/TryHackMe/WiFiHacking101/BSSID.PNG">

***--BSSID***


And to set the channel?

<img src="/images/TryHackMe/WiFiHacking101/Channel.PNG">

***--channel***


And how do you tell it to capture packets to a file?

<img src="/images/TryHackMe/WiFiHacking101/Write.PNG">

***-w***


TASK 3
----

What flag do we use to specify a BSSID to attack?

<img src="/images/TryHackMe/WiFiHacking101/B.PNG">

***-b***


What flag do we use to specify a wordlist?

<img src="/images/TryHackMe/WiFiHacking101/Word.PNG">

***-w***


How do we create a HCCAPX in order to use hashcat to crack the password?

<img src="/images/TryHackMe/WiFiHacking101/HCCAPX.PNG">

***-j***


Using the rockyou wordlist, crack the password in the attached capture. What's the password?

Now we get to do more than just read!

Lets extract the NinjaJc01-01.cap file into our Downloads folder

```cd Downloads```

now lets run aircrack-ng on the cap file!

```aircrack-ng NinjaJc01-01.cap -w /usr/share/wordlists/rockyou.txt```

<img src="/images/TryHackMe/WiFiHacking101/Pass.PNG">


***greeneggsandham***


Where is password cracking likely to be fastest, CPU or GPU? 

***GPU*** GPUs seems to be stroinger "powerhorses" when they can be used



<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
