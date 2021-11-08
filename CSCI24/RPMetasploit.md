---
layout: page
title: VulnNet: RPMetasploit
permalink: /CSCI24/RPMetasploit/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>


Task 2
---

This starts off with a simple question

start msfconsole without the banner (but why would you ever want that????)

***-q***

It then asks for the database it is using for MS5

***postgresql***

---
Task 3
---

The help menu has a very short one-character alias, what is it?

***?***


What is the base command we use for searching? 

***search***


what command we use to select it as the active module?

***use***


How about if we want to view information about either a specific module or just the active one we have selected?

***info***


Metasploit has a built-in netcat-like function where we can make a quick connection with a host simply to verify that we can 'talk' to it. What command is this? 

***connect***


Entirely one of the commands purely utilized for fun, what command displays the motd/ascii art we see when we start msfconsole (without -q flag)?

***banner***


We'll revisit these next two commands shortly, however, they're two of the most used commands within Metasploit. First, what command do we use to change the value of a variable?

***set***



Metasploit supports the use of global variables, something which is incredibly useful when you're specifically focusing on a single box. What command changes the value of a variable globally? 

***setg***


Now that we've learned how to change the value of variables, how do we view them? There are technically several answers to this question, however, I'm looking for a specific three-letter command which is used to view the value of single variables.

***get***




How about changing the value of a variable to null/no value?

***unset***




When performing a penetration test it's quite common to record your screen either for further review or for providing evidence of any actions taken. This is often coupled with the collection of console output to a file as it can be incredibly useful to grep for different pieces of information output to the screen. What command can we use to set our console output to save to a file?

***spool***



Leaving a Metasploit console running isn't always convenient and it can be helpful to have all of our previously set values load when starting up Metasploit. What command can we use to store the settings/active datastores from Metasploit to a settings file? This will save within your msf4 (or msf5) directory and can be undone easily by simply removing the created settings file. 

***save***


---
Task 4
---

Easily the most common module utilized, which module holds all of the exploit code we will use?

***exploit***


Used hand in hand with exploits, which module contains the various bits of shellcode we send to have executed following exploitation?

***payload***

Which module is most commonly used in scanning and verification machines are exploitable? This is not the same as the actual exploitation of course. 

***auxiliary***


One of the most common activities after exploitation is looting and pivoting. Which module provides these capabilities?

***post***


Commonly utilized in payload obfuscation, which module allows us to modify the 'appearance' of our exploit such that we may avoid signature detection?

***encoder***


Last but not least, which module is used with buffer overflow and ROP attacks?

***NOP***


Not every module is loaded in by default, what command can we use to load different modules? 

***load***



---
Task 5
---

Time to get into a machine!

They also show us a way to combine msfconsole with nmap!

```db_nmap -sV 10.10.254.99```

This sadly did nothing and I could not find the service without a guide

***msrpc***


What is the full path for our exploit that now appears on the msfconsole prompt? *This will include the exploit section at the start

***exploit/windows/http/icecast_header***


What is the name of the column on the far left side of the console that shows up next to 'Name'?

***#***




I could not get the exploits to work from here onward

---
Task 6
---

What's the name of the spool service? 

***



Let's go ahead and move into the spool process or at least attempt to! What command do we use to transfer ourselves into the process? This won't work at the current time as we don't have sufficient privileges but we can still try!

***


What command can we run to find out more information regarding the current user running the process we are in?

***


How about finding more information out about the system itself?

***


This might take a little bit of googling, what do we run to load mimikatz (more specifically the new version of mimikatz) so we can use it? 

***


Let's go ahead and figure out the privileges of our current user, what command do we run?

***


What command do we run to transfer files to our victim computer?

***


How about if we want to run a Metasploit module?

***


A simple question but still quite necessary, what command do we run to figure out the networking information and interfaces on our victim?

***


One quick extra question, what command can we run in our meterpreter session to spawn a normal system shell? 

***

---
Task 7
---















***
