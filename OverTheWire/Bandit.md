## Level 0
To get to level 0 we need to simply SSH into Bandit.
username:bandit0
password:bandit0 
```console
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
## Level 0 ====> Level 1
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH.
```console
bandit0@bandit0:~$ ls
readme
bandit0@bandit0:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
Now, from here type ```exit```  use SSH (on port 2220) to log into that level and continue the game
```console
ssh bandit1@bandit.labs.overthewire.org -p 2220 
```
## Level 1 ====> Level 2
```console
bandit1@bandit:~$ ls -a
- . .. .bash_logout .bashrc .profile
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Level 2 ====> Level 3
```console
bandit2@bandit:~$ ls 
spaces in this filename
bandit2@bandit:~$ cat ./spaces\ in\ this\ filename
aBZ0W%EmUfAf/kHTQeOwf8bauFJ2lAiG
```
## Level 3 ====> Level 4
```console
bandit3@bandit:~$ ls 
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls -a
. .. .hidden
bandit3@bandit:~$ cat ./.hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
## Level 4 ====> Level 5
```console
bandit4@bandit:~$ ls 
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~inhere$ ls -a
.   -file00 -file02 -file04 -file06 -file08 
..  -file01 -file03 -file05 -file07 -file09
bandit4@bandit:~inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
## Level 5 ====> Level 6
```console
bandit5@bandit:~$ ls 
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~inhere$ find -type f -size 1033c -perm /u=r
./maybehere07/.file2
bandit5@bandit:~inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl/jG1ApGSfjYKqJU
```
## Level 6 ====> Level 7
```console
bandit6@bandit:~$ find / -user bandit7 -group -bandit6 -size 33c 2>/dev/null
z7WtoNQU2XfjmMtWA8u%rN4vzqu4v99S
```
## Level 7 ====> Level 8
```console
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth       TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Level 8 ====> Level 9
```console
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ grep [a-zA-Z0-9] data.txt |sort| uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
# Level 9 ====> Level 10
```console
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep "="
ds=5
f============ theM
=XeOh
=vb
O=Nq
=I6a
============ password
============ is
2\.=
u=]T
%AM_9=
1~=y
Q=9(
j=GD
b=fF
0?F=(
.DX_/=
============ G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
# Level 10 ====> Level 11
```console
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt | base64 --decode
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBm
```
# Level 11 ====> Level 12
```console
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```

