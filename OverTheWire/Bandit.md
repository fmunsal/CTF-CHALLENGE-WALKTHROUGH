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
bandit0@bandit1:~$ ls -a
- . .. .bash_logout .bashrc .profile
bandit0@bandit1:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Level 2 ====> Level 3
```console
bandit0@bandit2:~$ ls 
spaces in this filename
bandit0@bandit2:~$ cat ./spaces\ in\ this\ filename
aBZ0W%EmUfAf/kHTQeOwf8bauFJ2lAiG
```
## Level 3 ====> Level 4
```console
bandit3@bandit4:~$ ls 
inhere
bandit3@bandit4:~$ cd inhere/
bandit3@bandit4:~$ ls -a
. .. .hidden
bandit3@bandit4:~$ cat ./.hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
## Level 4 ====> Level 5
```console
bandit4@bandit3:~$ ls 
inhere
bandit4@bandit3:~$ cd inhere/
bandit4@bandit3:~$ ls -a
.   -file00 -file02 -file04 -file06 -file08 \n
..  -file01 -file03 -file05 -file07 -file09
bandit4@bandit3:~$ file ./-*
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
bandit4@bandit3:~$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```