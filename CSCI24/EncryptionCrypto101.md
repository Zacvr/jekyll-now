---
layout: page
title: Encryption Crypto 101
permalink: /CSCI24/EncryptionCrypto101/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>

Task 2
---

Are SSH keys protected with a passphrase or a password?

***passphrase***


---


Task 3
---

What does SSH stand for?


***Secure Shell***


How do webservers prove their identity?

***Certificates***


What is the main set of standards you need to comply with if you store or process payment card details?

***PCI-DSS***


---


Task 4
---

Time for my single Python programming class to show me the power of the Modulo

What's 30 % 5?

***0***


What's 25 % 7

***4***


What's 118613842 % 9091

[Mini Web Tool to the rescue!](https://miniwebtool.com/modulo-calculator/)

***3565***


---


Task 5
---

Should you trust DES? Yea/Nay

***Nay***


What was the result of the attempt to make DES more secure so that it could be used for longer?

***Triple DES***


Is it ok to share your public key? Yea/Nay

***Yea***


---


Task 6
---

p*q=n

p = 4391, q = 6659. What is n?

***29239669***


---


Task 8
---

Who is TryHackMe's HTTPS certificate issued by?

By clicking the lock in Firefox > Clicking "Connection Secure" > Click "More Information > Finally Click "View Certificate" under the Security tab we can see the "Common Name"

***R3***


---


Task 9
---

What algorithm does the key use?

***RSA***


Crack the password with John The Ripper and rockyou, what's the passphrase for the key?

Finally we can open our VM to try some SSH2John

First lets install it

```wget https://raw.githubusercontent.com/magnumripper/JohnTheRipper/bleeding-jumbo/run/ssh2john.py```

```/usr/share/john/ssh2john.py idrsa.id_rsa > idrdsa.hash```

<img src="/images/CSCI24/EncryptionCrypto101/Task 9 SSH2John Install.png">

we now have a a giant string instead of the Key we had before

<img src="/images/CSCI24/EncryptionCrypto101/KeyToPass.png">

Now we can run John as we would normally

```sudo john --wordlist=/usr/share/wordlists/rockyou.txt idrsa.hash```

<img src="/images/CSCI24/EncryptionCrypto101/PassClear.png">

***delicious***


---


Task 11
---

You have the private key, and a file encrypted with the public key. Decrypt the file. What's the secret word?

After downloaidng the files lets import the key

```gpg --import tryhackme.key```

and now lets open the mesage 

```gpg --decrypt message.gpg > EasyGPG.txt```

<img src="/images/CSCI24/EncryptionCrypto101/GPG.png">


***Pineapple***
