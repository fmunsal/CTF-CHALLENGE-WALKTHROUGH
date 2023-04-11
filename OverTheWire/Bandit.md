## Level 0
To get to level 0 we need to simply SSH into Bandit.
username:bandit0
password:bandit0 
```
ssh bandit0@bandit.labs.overthewire.org -p 2220
```
## Level 0 ====> Level 1
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH.
```
bandit0@bandit0:~$ ls
readme
bandit0@bandit0:~$ cat readme
NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
Now, from here type ```exit```  use SSH (on port 2220) to log into that level and continue the game
```
ssh bandit1@bandit.labs.overthewire.org -p 2220 
```
## Level 1 ====> Level 2