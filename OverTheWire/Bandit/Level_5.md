---
layout: page
title: Bandit Level 5
permalink: /Tutorials/OTWBandit/Level_5/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 4](https://zacvr.github.io//Tutorials/OTWBandit/Level_4)
<br/>

Level 5 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit4@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"koReBOKuIDDepwhWk7jZC0RTdopnAYKh"
<br/>
We are now into level 4
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:
<br/>
human-readable
<br/>
1033 bytes in size
<br/>
not executable"
<br/><br/>
If you have done this before you will know you can use
<br/><br/>
"ls " to show files/folders
<br/><br/>
If we then "cd inhere"
<br/><br/>
To find the password we will need to find the correct file
<br/><br/>
"find . -type f -size 1033c ! -executable -exec file {} + | grep ASCII"
<br/><br/>
This will show "./maybeinhere07/.file2" as a suspect
<br/><br/>
Next we will
<br/><br/>
"cat maybehere07/.file2" to read the file
<br/><br/>
we will find the password
<br/><br/>
"DXjZPULLxYr17uwoI01bNLQbtFemEgo7"
<br/><br/>
Once again we can use
<br/>
"ssh bandit6@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 6](https://zacvr.github.io//Tutorials/OTWBandit/Level_6)
