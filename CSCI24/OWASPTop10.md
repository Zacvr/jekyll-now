---
layout: page
title: OWASP Top 10
permalink: /CSCI24/OWASPTop10/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>


Task 5
---

What strange text file is in the website root directory?

If we search with ls we will see the files in the root directory

```ls```

<img src="/images/CSCI24/OWASPTop10/Task 5 Q1.png">

***drpepper.txt***

How many non-root/non-service/non-daemon users are there?

```cat /etc/passwd```

***0***

What user is this app running as?

```whoami```

***www-data ***

What is the user's shell set as?

```cat /etc/passwd```

***/usr/sbin/nologin***

What version of Ubuntu is running?

```lsb_release -a```

***18.04.4***

Print out the MOTD.  What favorite beverage is shown?

```cat /etc/update-motd.d/00-header```

***Dr Pepper*** Shocker right?

Task 7
---

What is the flag that you found in darren's account?

***

Now try to do the same trick and see if you can login as arthur.

***

What is the flag that you found in arthur's account?

***

Task 11
---

What is the name of the mentioned directory?

***

Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data?

***

Use the supporting material to access the sensitive data. What is the password hash of the admin user?

***

Crack the hash.
What is the admin's plaintext password?

***

Login as the admin. What is the flag?

***

Task 13
---

Full form of XML

***

Is it compulsory to have XML prolog in XML documents?

***

Can we validate XML documents against a schema?

***

How can we specify XML version and encoding in XML document?

***

Task 14
---

How do you define a new ELEMENT?

***

How do you define a ROOT element?

***

How do you define a new ENTITY?

***

Task 16
---

What is the name of the user in /etc/passwd

***

Where is falcon's SSH key located?

***

What are the first 18 characters for falcon's private key

***

Task 18
---

Look at other users notes. What is the flag?

***

Task 19
---

Hack into the webapp, and find the flag!

***

Task 20
---

Navigate to http://MACHINE_IP/ in your browser and click on the "Reflected XSS" tab on the navbar; craft a reflected XSS payload that will cause a popup saying "Hello".

***

On the same reflective page, craft a reflected XSS payload that will cause a popup with your machines IP address.

***

Now navigate to http://MACHINE_IP/ in your browser and click on the "Stored XSS" tab on the navbar; make an account.

***

Then add a comment and see if you can insert some of your own HTML.

***

On the same page, create an alert popup box appear on the page with your document cookies.

***

Change "XSS Playground" to "I am a hacker" by adding a comment and using Javascript.

***

Task 21
---

Who developed the Tomcat application?

***

What type of attack that crashes services can be performed with insecure deserialization?

***

Task 22
---

Select the correct term of the following statement:
if a dog was sleeping, would this be:

A) A State
B) A Behaviour 

***

Task 23
---

What is the name of the base-2 formatting that data is sent across a network as? 

***

Task 24
---

If a cookie had the path of webapp.com/login , what would the URL that the user has to visit be?

***

What is the acronym for the web technology that Secure cookies work over?

***

Task 25
---

1st flag (cookie value)

***

2nd flag (admin dashboard)

***

Task 26
---

flag.txt

***

Task 29
---

How many characters are in /etc/passwd (use wc -c /etc/passwd to get the answer)

***

Task 30
---

What IP address is the attacker using?

***

What kind of attack is being carried out?

***
