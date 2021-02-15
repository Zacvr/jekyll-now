---
layout: page
title: Bandit Level 18
permalink: /Tutorials/OTWBandit/Level_18/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 17](https://zacvr.github.io//Tutorials/OTWBandit/Level_17)
<br/>

Level 18 Fight!
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit18@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd"
<br/>
Huh.. We got logged out!
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH."
<br/><br/>
For this level we know the location of the file
<br/><br/>
" ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme"
<br/><br/>
This will connect and read the file that has the password
<br/><br/>
We then type in the current password and hit enter
<br/><br/>
We get a message that says "IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x"
<br/><br/>
The password is "IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x"
<br/><br/>
Once again we can use
<br/>
"ssh bandit19@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 19](https://zacvr.github.io//Tutorials/OTWBandit/Level_19)
