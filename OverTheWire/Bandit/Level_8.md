---
layout: page
title: Bandit Level 8
permalink: /Tutorials/OTWBandit/Level_8/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 7](https://zacvr.github.io//Tutorials/OTWBandit/Level_7)
<br/>

Level 8 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit8@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"cvX2JJa4CFALtqS87jk27qwqGhBM9plV"
<br/>
We are now into level 8
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in the file data.txt and is the only line of text that occurs only once"
<br/><br/>
If you have done this before you will know you can use
<br/><br/>
"ls " to show files/folders
<br/><br/>
We then see"data.txt"
<br/><br/>
To find the password we will need to find the correct part of the txt file with
<br/><br/>
"cat data.txt | sort | uniq -u"
<br/><br/>
This will read the file/sort it/ and then find only single occurences
<br/><br/>
"UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR" is the password
<br/><br/>
Once again we can use
<br/>
"ssh bandit9@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 9](https://zacvr.github.io//Tutorials/OTWBandit/Level_9)
