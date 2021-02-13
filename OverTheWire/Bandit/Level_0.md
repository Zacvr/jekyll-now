---
layout: page
title: Bandit Level 0
permalink: /Tutorials/OTWBandit/Level_0/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
Level 01 Fight!
<br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/>
SSH Info
Host: bandit.labs.overthewire.org
Port: 2220
<br/>
Username:bandit0 
<br/>
Password:bandit0
<br/>
I use this specific line to type in each level 
<br/>
"ssh bandit0@bandit.labs.overthewire.org -p 2220" 
<br/>
Then just change the 0 for the level you want to type the password to
<br/>
Then use the password:bandit0
<br/>
Now we are into level 0
<br/>
If you us "ls" you will see a file named "readme"
<br/>
If you use "cat readme" you will get the password 
<br/>
"boJ9jbbUNNfktd78OOpsqOltutMc3MY1"
<br/>
then you can type in
<br/>
ssh bandit1@bandit.labs.overthewire.org -p 2220
and the password we just found to login to the next level
<br/>
[Next Level: 1](https://zacvr.github.io//Tutorials/OTWBandit/Level_1)
