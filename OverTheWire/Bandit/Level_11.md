---
layout: page
title: Bandit Level 11
permalink: /Tutorials/OTWBandit/Level_11/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 10](https://zacvr.github.io//Tutorials/OTWBandit/Level_10)
<br/><br/>

Level 11 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit11@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR"
<br/>
We are now into level 11
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in the file data.txt, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions"
<br/><br/>
If you have done this before you will know that is most likely ROT13
<br/><br/>
"ls " to show files/folders
<br/><br/>
We then see"data.txt"
<br/><br/>
To find the password we will need to find the correct part of the txt file with
<br/><br/>
"strings data.txt"
<br/><br/>
This will show the encoded password
<br/><br/>
We can use CyberChef or [My CipherSolver](https://github.com/Zacvr/CipherSolver)
<br/><br/>
We can then decode this into
<br/><br/>
"The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu"
<br/><br/>
"5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu" is the password
<br/><br/>
Once again we can use
<br/>
"ssh bandit12@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 12](https://zacvr.github.io//Tutorials/OTWBandit/Level_12)
