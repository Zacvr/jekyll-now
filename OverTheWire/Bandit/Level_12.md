---
layout: page
title: Bandit Level 12
permalink: /Tutorials/OTWBandit/Level_12/
---
[OverTheWire-Level Directory](https://zacvr.github.io/Tutorials/OTWBandit/)
<br/>
[Previous Level: 11](https://zacvr.github.io//Tutorials/OTWBandit/Level_11)
<br/>

Level 12 Fight!
<br/><br/>
In order to begin you will need to use PuTTY or preferably Linux and use the following information
<br/><br/>
If you are currently in a level type "logout"
<br/><br/>
Now type "ssh bandit9@bandit.labs.overthewire.org -p 2220"
<br/>
Password:"5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu"
<br/>
We are now into level 12
<br/><br/>
For this level we are told
<br/><br/>
"The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)"
<br/><br/>
If you have done this before you will know that is most likely ROT13
<br/><br/>
"ls " to show files/folders
<br/><br/>
We then see"data.txt"
<br/><br/>
To find the password we will need to copy this for modifications
<br/><br/>
"mkdir /tmp/bandit12" to create a tmp folder to work in
<br/><br/>
"cp data.txt /tmp/bandit12" copies "data.txt" into that folder
<br/><br/>
"cd /tmp/bandit12" moves into that folder
<br/><br/>
Next we should convert the hexdump into binary with "xxd"
<br/><br/>
"xxd -r data.txt data1.txt" will create a new hopefully Binary copy
<br/><br/>
Now we need to know the file type
<br/><br/>
"file data1.txt" will show us that it is a GZip file
<br/><br/>
"mv data1.txt data1.gz" will convert it to the proper format
<br/><br/>
"gzip -d data1.gz" will decompress the data
<br/><br/>
if we cat the data1 file it is still gibberish
<br/><br/>
"file data1" shows it as a bzip2 file
<br/><br/>
"mv data1 data1bz2" will convert it to a bzip2 file
<br/><br/>
"bzip2 -d data1.bz2" will decompress it again
<br/><br/>
This file will still be gibberish and is now a GZip file again
<br/><br/>
"mv data1.txt data1.gz" will convert it to the proper format
<br/><br/>
"gzip -d data1.gz" will decompress the data
<br/><br/>
Now it says it is a TAR archive
<br/><br/>
"mv data1 data1.tar"
<br/><br/>
"tar xvf data1.tar"
<br/><br/>
This will create a "data5.bin" file which is another TAR file
<br/><br/>
"mv data5 data5.tar"
<br/><br/>
"tar xvf data5.tar"
<br/><br/>
This will create a "data6.bin" file which is another BZip2 file
<br/><br/>
"mv data6.bin data6.bz2"
<br/><br/>
"bzip2 -d data6.bz2"
<br/><br/>
This will create a "data6" file which is another TAR file
<br/><br/>
"mv data6 data6.tar"
<br/><br/>
"tar xvf data6.tar"
<br/><br/>
This will create a "data6.bin" file which is another BZip2 file
<br/><br/>
"mv data6.bin data6.bz2"
<br/><br/>
"bzip2 -d data6.bz2"
<br/><br/>
This will create a "data6" file which is another TAR file
<br/><br/>
"mv data6 data6.tar"
<br/><br/>
"tar xvf data6.tar"
<br/><br/>
This will create a file named "data8.bin" which is a GZip file
<br/><br/>
"mv data8.bin data9.gz" will convert it to the proper format
<br/><br/>
"gzip -d data9.gz" will decompress the data
<br/><br/>
If we run "cat data9" WE FINALLY GET A PASSWORD!
<br/><br/>
"The password is 8ZjyCRiBWFYkneahHwxCv3wb2a1ORpYL"
<br/><br/>
Once again we can use
<br/>
"ssh bandit13@bandit.labs.overthewire.org -p 2220"
<br/>
and the password we just found to login to the next level
<br/><br/>
[Next Level: 13](https://zacvr.github.io//Tutorials/OTWBandit/Level_13)
