---
layout: page
title: Mobile Malware Analysis
permalink: /CSCI24/MMA/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>

Task 3
---

What known as the first malware created to affect mobile devices?

***Cabir***

What technology does this worm used to multiply?

***Bluetooth***

What operating system did it infect?

***Symbian

What message did it show on the screen of the infected mobile phone?

***Caribe***

---


Task 3
---

We are going to use the built in VM browser that opens in THM


What is the format of the file?




Decode the name of the sample.




Which is the target platform?



Task 4
---


What does Avast-Mobile can tell us about this software?




What program was used to create the malware?




What is the package name?





What is the SHA-1 signature?



What is the unique XML file?





How many permissions are there inside?




Which permission allows the application to take pictures with the camera?


What is the message left by the community?




Task 5
---





What is the programming language used to create the program?





How many signatures does the package has? 



Application is signed with v1 signature scheme, what is it vulnerable to on Android <7.0?





What is the App name?





It looks like  there is a function calling for the package manager, so it can see all the installed applications. What function is that?




Task 6
---



What is the SHA-256 hash of the file?




After finding the sample on VirusTotal, what does the "Avast" anti-virus engine recognizes it as?




With what we have, try to find out the name of the sample.




It seems like it is a very dangerous malware and has a big history of destruction.

This became news for spying journalists, what year was that?




If we search the name we found of the malware in MITRE ATT&CK (https://attack.mitre.org/), we can find some interesting information. 

What is the ID of the MITRE ATT&CK that is associated with our sample?





What technique has the ability to exploit OS vulnerabilities to escalate privileges? 




There is a permission that when accepted, allows the application to access the list of accounts in the Accounts Service. What is the status shown by MobSF regarding this permission. (android.permission.GET.ACCOUNTS)




What org.eclipse.paho.client file refers to properties of Portuguese from Brazil (pt-br)?






The malware has a special appeal for its safety and its internal components, reducing the risk of compromise. It has a functionality for its cryptographic operations with the feature of a random bit generation service. How can it be identified?























<br/><br/>
What networking constructs are used to direct traffic to the right application on a server?

***Ports***


How many of these are available on any network-enabled computer?

***65535***



[Research] How many of these are considered "well-known"? (These are the "standard" numbers mentioned in the task)

A quick google shows port 0-1023 as well known so

***1024***


Task 3
---

<br/><br/>
Time to use ```Nmap -H``` for our answers


What is the first switch listed in the help menu for a 'Syn Scan' (more on this later!)?

```nmap -h | grep scan```

<img src="/images/CSCI24/FurtherNMap/Task 3 Q1.png">

***-sS***

