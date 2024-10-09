# the roots 
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{g3jT7rqo6guc6OtN55YGo8xas5M.dhzN5QDL3EzN0czW}




# program and absolute path 

hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{4FbaY7ViynmV7I-e8bFjOmJvxIw.dVDN1QDL3EzN0czW}


# position-thy-self


hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/build-essential directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /usr/share/build-essential
hacker@paths~position-thy-self:/usr/share/build-essential$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{kZM-kSK2sgO7IE3FQzzo9Bc44Iu.dZDN1QDL3EzN0czW}



# position elsewhere


hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/67 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /proc/67
hacker@paths~position-elsewhere:/proc/67$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{Q6KANxhguF4ytUYAcgsglcsfBbb.ddDN1QDL3EzN0czW}




# position yet elsewhere


hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /usr/share/doc  
hacker@paths~position-yet-elsewhere:/usr/share/doc$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{gc3y5V6sQkV8j4zue95h-fWJGf5.dhDN1QDL3EzN0czW}



# implicit relative path 


hacker@paths~implicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{MvgLlgeQMXZL3WrxBu0VwcM47S2.dlDN1QDL3EzN0czW}




# relative path

hacker@paths~explicit-relative-paths-from-:~$ /challenge/run
Incorrect...
You are not currently in the / directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{EDKqE7tldxLkHyGC1CAlbIsYS8x.dBTN1QDL3EzN0czW}


# implicit relative path 



hacker@paths~implicit-relative-path:~$ /challenge/run
Incorrect...
You are not currently in the /challenge directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{UcY2tRsVfiJqmrO2Y5wcfuTMHWK.dFTN1QDL3EzN0czW}


# home sweet home 

hacker@paths~home-sweet-home:~$ /challenge/run ~/s
Writing the file to /home/hacker/s!
... and reading it back to you:
pwn.college{MrEpgIEJLXw0fU1byteFx07uVkk.dNzM4QDL3EzN0czW}
hacker@paths~home-sweet-home:~$ 
