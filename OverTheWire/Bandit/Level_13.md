---
layout: page
title: Bandit Level 13
permalink: /Tutorials/OTWBandit/Level_13/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 12](https://zacvr.github.io//Tutorials/OTWBandit/Level_12)
<br/>

Level 13 Fight!
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit13@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL"
<br/>
We are now into level 13
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost."
<br/><br/>
"ls " to show files/folders
<br/><br/>
We then see "sshkey.private"
<br/><br/>
lets try to login with this ssh key
<br/><br/>
We know the user is "bandit14" and the address is "local host" and even the key!
<br/><br/>
"ssh bandit14@localhost -i sshkey.private"
<br/><br/>
Lets look at that file path
<br/><br/>
"cat /etc/bandit_pass/bandit14"
<br/><br/>
It then shows us a password
<br/><br/>
"4wcYUJFw0k0XLShlDzztnTBHiqxU3b3e"
<br/><br/>
Once again we can use
<br/>
"ssh bandit14@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 14](https://zacvr.github.io//Tutorials/OTWBandit/Level_14)
