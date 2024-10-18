# permissions~changing-file-ownership

hacker@permissions~changing-file-ownership:~$ chown hacker /flag
hacker@permissions~changing-file-ownership:~$ cat /flag
pwn.college{wvDT8MOvyXNPVQ5BthV3JqAR9WG.dFTM2QDL3EzN0czW}
hacker@permissions~changing-file-ownership:~$ 

# permissions~groups-and-files

hacker@permissions~groups-and-files:~$ chgrp hacker /flag
hacker@permissions~groups-and-files:~$ cat /flag
pwn.college{sNiB77yZ3j3wlKk8ecu6f1lV94o.dFzNyUDL3EzN0czW}
hacker@permissions~groups-and-files:~$ 


# permissions~fun-with-groups-names

hacker@permissions~fun-with-groups-names:~$ id
uid=1000(hacker) gid=1000(grp9069) groups=1000(grp9069)
hacker@permissions~fun-with-groups-names:~$ chgrp 1000(grp9069) /flag
ssh-entrypoint: syntax error near unexpected token `('
hacker@permissions~fun-with-groups-names:~$ chgrp grp9069 /flag
hacker@permissions~fun-with-groups-names:~$ cat /flag
pwn.college{EdXcBwV5C_rOke_NDmtYGXhCKTT.dJzNyUDL3EzN0czW}
hacker@permissions~fun-with-groups-names:~$ 


