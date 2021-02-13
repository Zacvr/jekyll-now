---
layout: page
title: Bandit Level 3
permalink: /Tutorials/OTWBandit/Level_3/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 2](https://zacvr.github.io//Tutorials/OTWBandit/Level_2)
<br/>

Level 3 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit3@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK"
<br/>
We are now into level 2
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in a hidden file in the inhere directory."
<br/><br/>
If you have done this before you will know you can use
<br/><br/>
"ls -a" to show hidden files/folders
<br/><br/>
<br/><br/>
to find the password we will use
<br/><br/>
"cd inhere/" to go into the directory
<br/><br/>
Once inside we will use 
<br/><br/>
"ls -a" to show hidden files/folders again which shows a ".hidden" file
<br/><br/>
If we "cat .hidden"
<br/><br/>
we will find the password
<br/><br/>
"pIwrPrtPN36QITSp3EQaw936yaFoFgAB"
<br/><br/>
Once again we can use
<br/>
"ssh bandit4@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 4](https://zacvr.github.io//Tutorials/OTWBandit/Level_4)
