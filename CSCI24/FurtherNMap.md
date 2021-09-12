---
layout: page
title: Week 2 Lab
permalink: /CSCI24/FurtherNMap/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>

Task 2
---

<br/><br/>
What networking constructs are used to direct traffic to the right application on a server?

***Ports***
<br/><br/>
How many of these are available on any network-enabled computer?
<br/>
***65535***
<br/><br/>
[Research] How many of these are considered "well-known"? (These are the "standard" numbers mentioned in the task)
<br/>
A quick google shows port 0-1023 as well known so
<br/>
***1024***
<br/><br/>

Task 3
---

<br/><br/>
Time to use
***Nmap -H*** for our answers
<br/><br/>


What is the first switch listed in the help menu for a 'Syn Scan' (more on this later!)?
<br/>
```nmap -h | grep scan```
<br/>
<img src="/images/CSCI24/FurtherNMap/Task 3 Q1.png">
<br/>
***-sS***
<br/>


Which switch would you use for a "UDP scan"?
```nmap -h | grep UDP```
<br/>

<br/>
***-sU***
<br/>


If you wanted to detect which operating system the target is running on, which switch would you use?

<br/>
Nmap provides a switch to detect the version of the services running on the target. What is this switch?

<br/>
The default output provided by nmap often does not provide enough information for a pentester. How would you increase the verbosity?

<br/><br/>
Verbosity level one is good, but verbosity level two is better! How would you set the verbosity level to two?
(Note: it's highly advisable to always use at least this option)

<br/>
We should always save the output of our scans -- this means that we only need to run the scan once (reducing network traffic and thus chance of detection), and gives us a reference to use when writing reports for clients.

What switch would you use to save the nmap results in three major formats?

<br/>
What switch would you use to save the nmap results in a "normal" format?

<br/>
A very useful output format: how would you save results in a "grepable" format?

<br/>
Sometimes the results we're getting just aren't enough. If we don't care about how loud we are, we can enable "aggressive" mode. This is a shorthand switch that activates service detection, operating system detection, a traceroute and common script scanning.

How would you activate this setting?

<br/>
Nmap offers five levels of "timing" template. These are essentially used to increase the speed your scan runs at. Be careful though: higher speeds are noisier, and can incur errors!

How would you set the timing template to level 5?

<br/>
We can also choose which port(s) to scan.

How would you tell nmap to only scan port 80?

<br/>
How would you tell nmap to scan ports 1000-1500?

<br/>
A very useful option that should not be ignored:

How would you tell nmap to scan all ports?

<br/>
How would you activate a script from the nmap scripting library (lots more on this later!)?

<br/>
How would you activate all of the scripts in the "vuln" category?

<br/>
