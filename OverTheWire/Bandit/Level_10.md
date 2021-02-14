---
layout: page
title: Bandit Level 10
permalink: /Tutorials/OTWBandit/Level_10/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 9](https://zacvr.github.io//Tutorials/OTWBandit/Level_9)
<br/>

Level 10 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit9@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk"
<br/>
We are now into level 10
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in the file data.txt, which contains base64 encoded data"
<br/><br/>
If you have done this before you will know you can use
<br/><br/>
"ls " to show files/folders
<br/><br/>
We then see"data.txt"
<br/><br/>
To find the password we will need to find the correct part of the txt file with
<br/><br/>
"base64 data.txt"
<br/><br/>
This will show the encoded password
<br/><br/>
We can use CyberChef or [My CipherSolver](https://github.com/Zacvr/CipherSolver)
<br/><br/>
We can then decode this into
<br/><br/>
"VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg=="
<br/><br/>
This looks like normal Base64 now... Lets double decode it!
<br/><br/>
"IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR" is the password
<br/><br/>
Once again we can use
<br/>
"ssh bandit11@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 11](https://zacvr.github.io//Tutorials/OTWBandit/Level_11)
