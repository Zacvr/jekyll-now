---
layout: page
title: Bandit Level 19
permalink: /Tutorials/OTWBandit/Level_19/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 18](https://zacvr.github.io//Tutorials/OTWBandit/Level_18)
<br/>

Level 19 Fight!
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit19@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"IueksS7Ubh8G3DCwVzrTd8rAVOwq3M5x"
<br/>
We are now into level 19
<br/><br/>
For this level we are told
<br/><br/>
"To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary."
<br/><br/>
Lets try to run this file
<br/><br/>
"./bandit20-do "
<br/><br/>
This simple responds with
<br/><br/>
"Run a command as another user.
  Example: ./bandit20-do id
"
<br/><br/>
Lets try to cat the file we need
<br/><br/>
"./bandit20-do cat /etc/bandit_pass/bandit20"
<br/><br/>
We now simple get the password as a response
<br/><br/>
The password is "GbKksEFF4yrVs6il55v6gwY5aVje5f0j"
<br/><br/>
Once again we can use
<br/>
"ssh bandit20@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 20](https://zacvr.github.io//Tutorials/OTWBandit/Level_20)
