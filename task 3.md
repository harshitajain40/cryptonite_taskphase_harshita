# cat-not-the-pet-but-the-command
```
hacker@commands~cat-not-the-pet-but-the-command:~$ cat ~/flag
```
FLAG:pwn.college{MPyw8CEfXPXMaV6BfiXF0wlSjRF.dFzN1QDL3EzN0czW}


# catting-absolute-paths
```
hacker@commands~catting-absolute-paths:~$ cat /flag
```
FLAG : pwn.college{weF8skjf48o0mL7b_Er57L4JkZu.dlTM5QDL3EzN0czW}


# more catting practice 
```
You cannot use the 'cd' command in this level, and must retrieve the flag by 
absolute path. Plus, I hid the flag in a different directory! You can find it 
in the file /usr/share/enchant-2/flag. Go cat it out **without** cding into 
that directory!
hacker@commands~more-catting-practice:~$ cat /usr/share/enchant-2/flag
```
pwn.college{EII3wqDVDgnihV3yM2-qqUUw3Lv.dBjM5QDL3EzN0czW}


# grepping-for-a-needle-in-a-haystack
```
hacker@commands~grepping-for-a-needle-in-a-haystack:~$ grep pwn.college /challenge/data.txt
```
pwn.college{wvuw13MHcwqwS33MoQsUkDBNf0z.ddTM4QDL3EzN0czW}


# commands~listing-files
```
hacker@commands~listing-files:~$ ls /challenge
30948-renamed-run-19834  DESCRIPTION.md
hacker@commands~listing-files:~$ /challenge/30948-renamed-run-19834
```
Yahaha, you found me! Here is your flag:
pwn.college{Yx2igdrY45x6n8G-uhLyR8mCT3-.dhjM4QDL3EzN0czW}


# touching-files
```
hacker@commands~touching-files:~$ cd /tp
ssh-entrypoint: cd: /tp: No such file or directory
hacker@commands~touching-files:~$ cd /tmp
hacker@commands~touching-files:/tmp$ touch pwn
hacker@commands~touching-files:/tmp$ touch college
hacker@commands~touching-files:/tmp$ /challenge/run
```
Success! Here is your flag:
pwn.college{oIaWsDI_JPbIEEF1MPABiNSa-Yd.dBzM4QDL3EzN0czW}


# removing files
```
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
```
Excellent removal. Here is your reward:
pwn.college{4evmFXbRIPx6-SsU41QLsFZRFw9.dZTOwUDL3EzN0czW}


# hidden-files
```
hacker@commands~hidden-files:~$ cd /
hacker@commands~hidden-files:/$ ls -a
.  ..  .dockerenv  .flag-11513123009445  bin  boot  challenge  dev  etc  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~hidden-files:/$ cat /.flag-11513123009445
```
pwn.college{w1ENm5t_AR11Ou7bTve23pDfUOi.dBTN4QDL3EzN0czW}


# an-epic-filesystem-ques
```
hacker@commands~an-epic-filesystem-quest:~$ cd /
hacker@commands~an-epic-filesystem-quest:/$ ls
WHISPER  bin  boot  challenge  dev  etc  flag  home  lib  lib32  lib64  libx32  media  mnt  nix  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
hacker@commands~an-epic-filesystem-quest:/$ cat WHISPER
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/sound/pci/lola
hacker@commands~an-epic-filesystem-quest:/$ cd
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/linux/linux-5.4/sound/pci/lola
DISPATCH  Makefile  built-in.a  lola.c  lola.h  lola_clock.c  lola_mixer.c  lola_pcm.c  lola_proc.c
hacker@commands~an-epic-filesystem-quest:~$ cat DISPATCH 
cat: DISPATCH: No such file or directory
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/linux/linux-5.4/sound/pci/lola/DISPATCH
Congratulations, you found the clue!
The next clue is in: /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag/__pycache__

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:~$ ls  /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag/__pycache__
DOSSIER-TRAPPED  __init__.cpython-38.pyc  flag.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:~$ cat  /opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag/__pycache__/DOSSIER-TRAPPED
Congratulations, you found the clue!
The next clue is in: /opt/linux/linux-5.4/arch/s390/boot

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:~$ ls /opt/linux/linux-5.4/arch/s390/boot
CUE-TRAPPED  boot.h      ctype.c   head_kdump.S  ipl_report.c  machine_kexec_reloc.c  pgm_check_info.c   string.c    version.c
Makefile     cmdline.c   ebcdic.c  install.sh    ipl_vmparm.c  mem.S                  sclp_early_core.c  text_dma.S
als.c        compressed  head.S    ipl_parm.c    kaslr.c       mem_detect.c           startup.c          uv.c
hacker@commands~an-epic-filesystem-quest:~$ cat /opt/linux/linux-5.4/arch/s390/boot/CUE-TRAPPED 
Great sleuthing!
The next clue is in: /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/TeX/Main/Italic
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/TeX/Main/Italic
CombDiacritMarks.js  GeneralPunctuation.js  Latin1Supplement.js  LetterlikeSymbols.js  Main.js  NOTE
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/share/javascript/mathjax/jax/output/HTML-CSS/fonts/TeX/Main/Italic/NOTE
Yahaha, you found me!
The next clue is in: /usr/share/racket/collects/racket/lang
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/share/racket/collects/racket/lang
BRIEF  compiled  reader.rkt
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/share/racket/collects/racket/lang/BRIEF
Tubular find!
The next clue is in: /usr/share/doc/libglib2.0-0

Watch out! The next clue is **trapped**. You'll need to read it out without 'cd'ing into the directory; otherwise, the clue will self destruct!
hacker@commands~an-epic-filesystem-quest:~$ ls /usr/share/doc/libglib2.0-0
INSIGHT-TRAPPED  NEWS.gz  README.md.gz  changelog.Debian.gz  copyright
hacker@commands~an-epic-filesystem-quest:~$ cat /usr/share/doc/libglib2.0-0/INSIGHT-TRAPPED 
Tubular find!
The next clue is in: /usr/local/lib/python3.8/dist-packages/scapy/contrib/automotive/obd/pid/__pycache__

The next clue is **hidden** --- its filename starts with a '.' character. You'll need to look for it using special options to 'ls'.
hacker@commands~an-epic-filesystem-quest:~$ ls -a  /usr/local/lib/python3.8/dist-packages/scapy/contrib/automotive/obd/pid/__pycache__
.   .SECRET                  pids.cpython-38.pyc        pids_20_3F.cpython-38.pyc  pids_60_7F.cpython-38.pyc  pids_A0_C0.cpython-38.pyc
..  __init__.cpython-38.pyc  pids_00_1F.cpython-38.pyc  pids_40_5F.cpython-38.pyc  pids_80_9F.cpython-38.pyc
hacker@commands~an-epic-filesystem-quest:~$ cat  /usr/local/lib/python3.8/dist-packages/scapy/contrib/automotive/obd/pid/__pycache__/.SECRET
Yahaha, you found me!
The next clue is in: /opt/linux/linux-5.4/include/config/split

The next clue is **delayed** --- it will not become readable until you enter the directory with 'cd'.
hacker@commands~an-epic-filesystem-quest:~$ cd /opt/linux/linux-5.4/include/config/split
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/split$ ls
ALERT  ptlock
hacker@commands~an-epic-filesystem-quest:/opt/linux/linux-5.4/include/config/split$ cat ALERT
```
CONGRATULATIONS! Your perserverence has paid off, and you have found the flag!
It is: pwn.college{IF56lxYOV2V4au4aeq7q4dyZTm5.dljM4QDL3EzN0czW}


# making-directories
```
hacker@commands~making-directories:~$ cd /tmp
hacker@commands~making-directories:/tmp$ mkdir pwn
hacker@commands~making-directories:/tmp$ ls
bin  hsperfdata_root  pwn  tmp.XvrUsDZh8M
hacker@commands~making-directories:/tmp$ cd pwn 
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ ls
college
hacker@commands~making-directories:/tmp/pwn$ ls /tmp/pwn/college
/tmp/pwn/college
/tmp/pwn/college
ssh-entrypoint: /tmp/pwn/college: Permission denied
hacker@commands~making-directories:/tmp/pwn$ ls  /tmp/pwn/college
/tmp/pwn/college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
```
Success! Here is your flag:
pwn.college{ctbcgfuW5A_Vvf9MKdAvaN9vbEm.dFzM4QDL3EzN0czW}




# finding files
```
hacker@commands~finding-files:~$ find /-name flag
find: ‘/-name’: No such file or directory
find: ‘flag’: No such file or directory
hacker@commands~finding-files:~$ find / -name flag
find: ‘/root’: Permission denied
find: ‘/proc/1/task/1/fd’: Permission denied
find: ‘/proc/1/task/1/fdinfo’: Permission denied
find: ‘/proc/1/task/1/ns’: Permission denied
find: ‘/proc/1/fd’: Permission denied
find: ‘/proc/1/map_files’: Permission denied
find: ‘/proc/1/fdinfo’: Permission denied
find: ‘/proc/1/ns’: Permission denied
find: ‘/proc/7/task/7/fd’: Permission denied
find: ‘/proc/7/task/7/fdinfo’: Permission denied
find: ‘/proc/7/task/7/ns’: Permission denied
find: ‘/proc/7/fd’: Permission denied
find: ‘/proc/7/map_files’: Permission denied
find: ‘/proc/7/fdinfo’: Permission denied
find: ‘/proc/7/ns’: Permission denied
find: ‘/var/log/private’: Permission denied
find: ‘/var/log/apache2’: Permission denied
find: ‘/var/log/mysql’: Permission denied
find: ‘/var/cache/ldconfig’: Permission denied
find: ‘/var/cache/apt/archives/partial’: Permission denied
find: ‘/var/cache/private’: Permission denied
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/php/sessions’: Permission denied
find: ‘/var/lib/mysql-files’: Permission denied
find: ‘/var/lib/private’: Permission denied
find: ‘/var/lib/mysql-keyring’: Permission denied
find: ‘/var/lib/mysql’: Permission denied
find: ‘/tmp/tmp.XvrUsDZh8M’: Permission denied
find: ‘/run/mysqld’: Permission denied
find: ‘/run/sudo’: Permission denied
find: ‘/etc/ssl/private’: Permission denied
/usr/local/lib/python3.8/dist-packages/pwnlib/flag
/usr/local/share/radare2/5.9.5/flag
/usr/lib/llvm-10/include/polly/flag
/opt/pwndbg/.venv/lib/python3.8/site-packages/pwnlib/flag
/opt/radare2/libr/flag
/nix/store/pmvk2bk4p550w182rjfm529kfqddnvh3-python3.11-pwntools-4.12.0/lib/python3.11/site-packages/pwnlib/flag
/nix/store/1yagn5s8sf7kcs2hkccgf8d0wxlrv5sz-radare2-5.9.0/share/radare2/5.9.0/flag
hacker@commands~finding-files:~$ cat /usr/local/lib/python3.8/dist-packages/pwnlib/flag
cat: /usr/local/lib/python3.8/dist-packages/pwnlib/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/local/share/radare2/5.9.5/flag
cat: /usr/local/share/radare2/5.9.5/flag: Is a directory
hacker@commands~finding-files:~$ cat /usr/lib/llvm-10/include/polly/flag
```
pwn.college{QbdJyYKy2QFTZkbQEtkCUyeEgRv.dJzM4QDL3EzN0czW}hacker@commands~finding-files:~$ 

# linking files
```
hacker@commands~linking-files:~$  ln -s /flag /home/hacker/not-the-flag
hacker@commands~linking-files:~$ /challenge/catflag
```
About to read out the /home/hacker/not-the-flag file!
pwn.college{cMR_Q3Yn1UGuu-0koexYsnuhwGC.dlTM1UDL3EzN0czW}


