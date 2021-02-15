---
layout: page
title: Bandit Level 17
permalink: /Tutorials/OTWBandit/Level_17/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 16](https://zacvr.github.io//Tutorials/OTWBandit/Level_16)
<br/>

Level 17 Fight!
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit17@bandit.labs.overthewire.org -p 2220 -i Bandit17.key"
<br/><br/>
We are told that the permissons are "too open"
<br/><br/>
I guess we can restrict them a bit huh?
<br/><br/>
"sudo chmod 400 bandit17.key"
<br/><br/>
Type in your actual sudo password and hit enter
<br/><br/>
This will protect a file against accidental overwriting.
<br/><br/>
We are now into level 17
<br/><br/>
For this level we are told
<br/><br/>
"There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new"
<br/><br/>
For this level we need to find the difference in 2 files
<br/><br/>
we can easily do this with "diff"
<br/><br/>
"diff passwords.new passwords.old"
<br/><br/>
This shows 2 possibilities
<br/><br/>
"
42c42
> kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd
---
< w0Yfolrc5bwjS4qw5mq1nnQi6mF03bii
"
<br/><br/>
We can try both of these for the next level or
<br/><br/>
The password is "kfBf3eYk5BPBRzwjqutbbfE887SVc5Yd"
<br/><br/>
Once again we can use
<br/>
"ssh bandit18@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 18](https://zacvr.github.io//Tutorials/OTWBandit/Level_18)
