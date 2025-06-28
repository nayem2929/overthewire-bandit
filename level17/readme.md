# Bandit Level17 Solution

**Objective:** Find the difference between 2 files to get the password.

**Commands Used:**
* `diff`: To compare two files and find the difference.
* `grep`: To filter the output from diff and only print the differences in the first file.

**Steps:**
1.  Use `cd bandit-repo/overthewire-bandit/level16` to navigate to the folder containing the RSA key for login.
2.  Use `ssh -i bandit17_key bandit17@bandit.labs.overthewire.org -p 2220` to login as user `bandit17` using the RSA key as 
   identity file.
3.  Once logged in, use `ls` to find the passwords.new and passwords.old files.
4.  Use `diff passwords.new passwords.old | grep '<'` to find the difference in the first file.
5.  This will print the password. 

**Password for Level 18:** x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
 

