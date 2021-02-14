---
layout: page
title: Bandit Level 9
permalink: /Tutorials/OTWBandit/Level_9/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 8](https://zacvr.github.io//Tutorials/OTWBandit/Level_8)
<br/>

Level 9 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit8@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR"
<br/>
We are now into level 8
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in the file data.txt in one of the few human-readable strings, preceded by several ‘=’ characters."
<br/><br/>
If you have done this before you will know you can use
<br/><br/>
"ls " to show files/folders
<br/><br/>
We then see"data.txt"
<br/><br/>
To find the password we will need to find the correct part of the txt file with
<br/><br/>
"strings data.txt | grep -E "=""
<br/><br/>
This will be a bit "dirty but we can see a string that should be the password
<br/><br/>
"truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk" is the password
<br/><br/>
Once again we can use
<br/>
"ssh bandit10@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 10](https://zacvr.github.io//Tutorials/OTWBandit/Level_10)
