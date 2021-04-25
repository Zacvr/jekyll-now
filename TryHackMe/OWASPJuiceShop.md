---
layout: page
title: OWASPJuiceShop
permalink: /Tutorials/TryHackMe/OWASPJuiceShop/
---

[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
<br/><br/>
<br/><br/>
<br/><br/>
Flags will be **BOLD**
<br/><br/>
<br/><br/>
<br/><br/>


LETS GET SOME JUICE!
----

First lets find the correct IP

```nmap -n -sn 10.10.175.0-255```

Since we know this is a website we can test all of our choices that have ports 80 & 443

<img src="/images/TryHackMe/OWASPJuiceShop/IPs.PNG">

Since 10.10.175.250 ONLY has HTTP lets try that in a browser

And for myself at least that was correct!

TASK 2
----

All of these answers are shown in THM

Question 1
***admin@juice-sh.op***

Question 2
***q***

Question 3
***Star Trek***

TASK 3
----

Looks like we need to break into the admin account

lets click on the "Account" button in the top right

Click "Login"

Lets type in some information for the username and password

<img src="/images/TryHackMe/OWASPJuiceShop/Admin.PNG">

Now lets change the email from "zac" to

```' or 1=1--```

<img src="/images/TryHackMe/OWASPJuiceShop/AdminPass.PNG">

Question 1
***32a5e0f21372bcc1000a6088b93b458e41f0e02a***

Alright now we need to get into Benders account

Lets go back to the login page and put

```bender@juice-sh.op'--``` as the email and anything for a password

<img src="/images/TryHackMe/OWASPJuiceShop/Bender.PNG">

Success! we did not even need to intercept the package since the email is valid and "--" will bypass the login system

<img src="/images/TryHackMe/OWASPJuiceShop/BenderPass.PNG">


We got in!


<img src="/images/TryHackMe/OWASPJuiceShop/Admin-Done.PNG">

**fb364762a3c102b2db932069c0e6b78e738d4066**


TASK 4
---

Now we need to use some brute forcing

First lets logout

Now lets put 

```admin@juice-sh.op```

as the email

Click "Action" and the "Send To Intruder"

Lets click on Intruder next to Proxy in Burpsuite

We are told to click "Clear §"

then click "Add §" twice inside of the password

Now lets click Payloads and load the requested payload

I had to install Seclists with

```sudo apt-get install seclists``` on my VM

After it is loaded lets click "Start attack"

Due to the demo version of Intruder it took awhile for me to find the correct password

"admin123" is the correct password (I should have guessed..)

<img src="/images/TryHackMe/OWASPJuiceShop/Admin123.PNG">

Now we have the answer to Question 1

<img src="/images/TryHackMe/OWASPJuiceShop/PasswordStrength.PNG">

**c2110d06dc6f81c67cd8099ff0ba601241f1ac0e**

Now we need to try and reset the password for "jim@juice-sh.op"

For our secuirty question wejust need to find it from the information provided in THM

It is most likely

```Samuel```

Lets try to set a new password

I set it to "12345"

<img src="/images/TryHackMe/OWASPJuiceShop/JimPass.PNG">

We now have the answer to Question 2!

**094fbc9b48e525150ba97d05b942bbf114987257**

Time for 

TASK 5
---







***169940f83378cc420ae4fdeb9c1f73631a2baee6***










<br/><br/>
[TryHackMe Directory](https://zacvr.github.io/Tutorials/TryHackMe/)
