---
layout: page
title: Bandit Level 15
permalink: /Tutorials/OTWBandit/Level_15/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 14](https://zacvr.github.io//Tutorials/OTWBandit/Level_14)
<br/>

Level 15 Fight!
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit15@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"BfMYroe26WYalil77FoDi9qh59eK5xNr"
<br/>
We are now into level 15
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL encryption."
<br/><br/>
For this level we need to use OpenSSL to connect to port 30001 and send the password
<br/><br/>
"openssl s_client -ign_eof -connect localhost:30001"
<br/><br/>
The "s_client" creates a generic SSL/TLS client which connects to the localhost on the typed in port
<br/><br/>
We then type in the current password and hit enter
<br/><br/>
We get a message that says "Correct!" with the password
<br/><br/>
The password is "cluFn7wTiGryunymYOu4RcffSxQluehd"
<br/><br/>
Once again we can use
<br/>
"ssh bandit16@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 16](https://zacvr.github.io//Tutorials/OTWBandit/Level_16)
