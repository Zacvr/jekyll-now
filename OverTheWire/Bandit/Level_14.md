---
layout: page
title: Bandit Level 14
permalink: /Tutorials/OTWBandit/Level_14/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 13](https://zacvr.github.io//Tutorials/OTWBandit/Level_13)
<br/>

Level 14 Fight!
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit14@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e"
<br/>
We are now into level 14
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost."
<br/><br/>
For this level we can use echo and NetCat aka "nc"
<br/><br/>
"echo 4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e | nc localhost 30000"
<br/><br/>
This will pop up with
<br/><br/>
"Correct!
BfMYroe26WYalil77FoDi9qh59eK5xNr"
<br/><br/>
The password is "BfMYroe26WYalil77FoDi9qh59eK5xNr"
<br/><br/>
Once again we can use
<br/>
"ssh bandit15@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 15](https://zacvr.github.io//Tutorials/OTWBandit/Level_15)
