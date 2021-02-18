---
layout: page
title: OpenVPN
permalink: /Tutorials/TryHackMe/OpenVPN/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
<br/><br/>
From this point onward we (I) will be using a Kali Linux VM for these challenges
<br/>
This is a simple tutorial for getting this to work
<br/>
First we will open a terminal and type
<br/>
"sudo apt install openvpn"
<br/>
We will then type in our actual password for sudo
<br/>
New we go to
<br/>
"[TryHackMe Access](https://tryhackme.com/access)"
<br/>
Next we need to download our Configuration File on the mid right of the screen
<br/>
We then will need to find the location of the download (For me it was in my downloads (Who would have guessed right?))
<br/>
Now we use the simple command they gave 
<br/>
"sudo openvpn /path-to-file/file-name.ovpn"
<br/>
Which in my case is "/home/kali/Downloads/ZacvrV2.ovpn"
<br/>
so I type in "sudo openvpn /home/kali/Downloads/ZacvrV2.ovpn"
<br/>
Now we are connected!
<br/>
For task 6 we need to deploy the machine
<br/>
After we click "Deploy Machine" we may need to wait for it to open all the way (and for the IP)
<br/>
Once we see the IP we can connect to the IP (via a web browser)
<br/>
It will be just the IP for me that was "10.10.118.109"
<br/>
It will show a page along with our flag!
<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
