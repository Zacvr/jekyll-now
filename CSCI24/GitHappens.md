---
layout: page
title: GitHappens
permalink: /CSCI24/GitHappens/
---

---

[CSCI 24 Directory](https://zacvr.github.io/CSCI24/)
<br/>

---
<br/>

Can you find the password to the application?
---

Looks like we are given a grey box with only an IP and "version control" as a hint

With a quick scan

```nmap -sV 10.10.118.209```

All we see is port 80 having a "nginx 1.14.0" running

Lets try looking for a Git repo shall we?

```nmap -A 10.10.118.209```

<img src="/images/CSCI24/GitHappens/Repo Found.png">

now if we go to

```http://10.10.118.209/``` 

We see a website with a login BUT if we go to

```10.10.118.209:80/.git/```

we can get all the files that we can manually but why not find a script someone has already made to speed up the process?

[Git-Dumper](sudo pip install git-dumper)

Now we need to install the Git-Dumper

```sudo pip install git-dumper```

Now lets downlaod the files

```git-dumper http://10.10.118.209:80/.git  ~/Here```

If you cat the README.md

you find the easter egg "git-fail

Sometimes, bad things happen to good sites"

If we cat the index we find a script at the bottom that we need to decode

Orrrr not?

okay well if we go to 

```git log``` while in ~/Here we see the commits mad to the git

after some googling we can go to specific commits of the git

<img src="/images/CSCI24/GitHappens/Commits.png">

```sudo git checkout 395e087334d613d5e423cdf8f7be27196a360459```

Lets look at the index again

```cat index.html```

<img src="/images/CSCI24/GitHappens/Password.png">


Find the Super Secret Password

***Th1s_1s_4_L0ng_4nd_S3cur3_P4ssw0rd!***

