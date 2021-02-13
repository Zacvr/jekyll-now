---
layout: page
title: Bandit Level 6
permalink: /Tutorials/OTWBandit/Level_6/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 5](https://zacvr.github.io//Tutorials/OTWBandit/Level_5)
<br/>

Level 6 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit4@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"DXjZPULLxYr17uwoI01bNLQbtFemEgo7"
<br/>
We are now into level 4
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored somewhere on the server and has all of the following properties:
<br/>
owned by user bandit7
<br/>
owned by group bandit6
<br/>
33 bytes in size"
<br/><br/>
To find the password we will need to find the correct file
<br/><br/>
"find / -user bandit7 -group bandit6 -size 33c"
<br/><br/>
This will show "/var/lib/dpkg/info/bandit7.password" as a suspect
<br/><br/>
Next we will
<br/><br/>
"cat /var/lib/dpkg/info/bandit7.password" to read the file
<br/><br/>
we will find the password
<br/><br/>
"HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs"
<br/><br/>
Once again we can use
<br/>
"ssh bandit7@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 7](https://zacvr.github.io//Tutorials/OTWBandit/Level_7)
