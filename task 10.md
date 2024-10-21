# root-with-su
```
hacker@users~becoming-root-with-su:~$ su
Password: 
root@users~becoming-root-with-su:/home/hacker# cat /flag
```
pwn.college{A35k62Uh-1nwMcvs8nyo3cqlXeE.dVTN0UDL3EzN0czW}


# other-users-with-su
```
hacker@users~other-users-with-su:~$ su zardus
Password: 
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
```
Congratulations, you have become Zardus! Here is your flag:
pwn.college{kFl2sRCmTewZkcgR_ZKeOID7SG9.dZTN0UDL3EzN0czW}


# cracking-passwords
```
hacker@users~cracking-passwords:~$ john /challenge/shadow-leak
Created directory: /home/hacker/.john
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:08 85% 1/3 0g/s 285.5p/s 285.5c/s 285.5C/s Zardus1111..z99999123456
0g 0:00:00:13 0% 2/3 0g/s 283.9p/s 283.9c/s 283.9C/s bigdog..francesco
0g 0:00:00:15 0% 2/3 0g/s 285.0p/s 285.0c/s 285.0C/s deedee..grizzly
0g 0:00:00:16 0% 2/3 0g/s 285.5p/s 285.5c/s 285.5C/s national..rocket1
0g 0:00:00:17 1% 2/3 0g/s 286.0p/s 286.0c/s 286.0C/s 1234qwer..babygirl
0g 0:00:00:17 1% 2/3 0g/s 286.4p/s 286.4c/s 286.4C/s katrina..karla
0g 0:00:00:19 1% 2/3 0g/s 286.7p/s 286.7c/s 286.7C/s 10sne1..nermal
aardvark         (zardus)
1g 0:00:00:20 100% 2/3 0.04847g/s 282.2p/s 282.2c/s 282.2C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password: 
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
```
Congratulations, you have become Zardus! Here is your flag:
pwn.college{M9l91JttQfQ2g-3n79jZlTgJzGq.ddTN0UDL3EzN0czW}

# using sudo 
```
hacker@users~using-sudo:~$ sudo cat /flag
```
pwn.college{EJL1n2bZ1KbyO2MtUnni6kyQK4v.dhTN0UDL3EzN0czW}




