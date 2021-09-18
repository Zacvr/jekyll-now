---
layout: page
title: Mobile Malware Analysis
permalink: /CSCI24/MMA/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>

Task 3
---

What known as the first malware created to affect mobile devices?

***Cabir***

What technology does this worm used to multiply?

***Bluetooth***

What operating system did it infect?

***Symbian***

What message did it show on the screen of the infected mobile phone?

***Caribe***

---


Task 3
---

We are going to use the built in VM browser that opens in THM


What is the format of the file?

***.APK***


Decode the name of the sample.

We will use hURL to decode (you can also use CyberChef)

```hURL -b "TWFsd2FyZQ"```

<img src="/images/CSCI24/MMA/Task 3 Q4.png">


***Malware***


Which is the target platform?

If we scroll down we can see "Android" listed in various places

***Android***

---

Task 4
---

We need to get the has with "Get-FileHash" or from within MobSF

<img src="/images/CSCI24/MMA/Task 4 Q1.png">

Our hash is "E201A1D2CECF1D04D97D59ABEC0863C716DCF9FCAD89B85D036F9163A48057E7"

Lets go to Virus Total and search the has!

What does Avast-Mobile can tell us about this software?

***Android:Metasploit-G [PUP]***

***For this answer AVAST was the answer not Avast-Mobile***


What program was used to create the malware?

***metasploit***


What is the package name?

***com.metasploit.stage***


What is the SHA-1 signature?

***74d442594acf11dc6e3492ffea5eb8956afd000d***


What is the unique XML file?

***AndroidManifest.xml***



How many permissions are there inside?

If we click the SHA-256 of that XML file it will show it has 22 permissions

***22***


Which permission allows the application to take pictures with the camera?

***android.permission.CAMERA***


What is the message left by the community?

***THM{V1ru5-T0t4al-TWFsd2FyZS1BbmFseXNpcw}***


---

Task 5
---

Due to the pain and suffering of a Windows VM in a Kali VM I installed MobSF


```sudo apt install python3-dev python3-venv python3-pip build-essential libffi-dev libssl-dev libxml2-dev libxslt1-dev  zlib1g-dev wkhtmltopdf```
```git clone https://github.com/MobSF/Mobile-Security-Framework-MobSF.git```
```cd Mobile-Security-Framework-MobSF```
```./setup.sh```

cd Mobile-Security-Framework-MobSF/
git pull origin master
. venv/bin/activate
pip install --no-cache-dir --use-deprecated=legacy-resolver -r requirements.txt
python manage.py makemigrations
python manage.py makemigrations StaticAnalyzer
python manage.py migrate
deactivate


this all did not work so back to the joys of a VM inception


What is the programming language used to create the program?

***Java***


How many signatures does the package has? 

***1***


Application is signed with v1 signature scheme, what is it vulnerable to on Android <7.0?

A  quick google search teaches about "Janus"

***Janus***


What is the App name?

***MainActivity***


It looks like  there is a function calling for the package manager, so it can see all the installed applications. What function is that?

If we look into the Java code we see

***b.getPackageManager***


Returning to the manifest.

The flag "android:allowBackup" allows the user to backup application data via USB debugging. It is recommended that this be set as "False", even if by default it is "True".

What is the severity of this configuration?

***Medium***


---

Task 6
---

Time to check into sample2.apk

What is the SHA-256 hash of the file?

***bd8cda80aaee3e4a17e9967a1c062ac5c8e4aefd7eaa3362f54044c2c94db52a***


After finding the sample on VirusTotal, what does the "Avast" anti-virus engine recognizes it as?

***Android:Obfus-BM [Trj]***


With what we have, try to find out the name of the sample.

Near the top of VirusTotal we see "Pegasus"

***Pegasus***


It seems like it is a very dangerous malware and has a big history of destruction.

This became news for spying journalists, what year was that?

***2017***


If we search the name we found of the malware in MITRE ATT&CK (https://attack.mitre.org/), we can find some interesting information. 

What is the ID of the MITRE ATT&CK that is associated with our sample?

Lets search "Pegasus" and look for an android based link

***S0316***


What technique has the ability to exploit OS vulnerabilities to escalate privileges? 

***T1404***


There is a permission that when accepted, allows the application to access the list of accounts in the Accounts Service. What is the status shown by MobSF regarding this permission. (android.permission.GET.ACCOUNTS)

***Dangerous***


What org.eclipse.paho.client file refers to properties of Portuguese from Brazil (pt-br)?

***org/eclipse/paho/client/mqttv3/internal/nls/messages_pt_BR.properties***


The malware has a special appeal for its safety and its internal components, reducing the risk of compromise. It has a functionality for its cryptographic operations with the feature of a random bit generation service. How can it be identified?

The Hint tells us to look into NIAP analysis, after some searching in the sidebar under "Secuirty Analysis" we can find it

***FCS_RBG_EXT.1.1***
