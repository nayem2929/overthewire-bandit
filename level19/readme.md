# Bandit Level19 Solution

**Objective:** To use setuid and read the password file as bandit20.

**Commands Used:**
* `ls`: To list the files and contents.
*`cat`: To read the password file.

**Steps:**
1.  Use `ssh bandit19@bandit.labs.overthewire.org -p 2220` to login as user `bandit19`.
2.  Use `ls -l` to list the **bandit20-do** file with it's permissions.
3.  Notice the s-bit in the place of users executable permission bit and the owner is bandit20. This means that this 
   is the exectuable that will give us elevated priviledge to execute commands as bandit20.
4.  Use `/home/bandit19/bandit20-do cat /etc/bandit_pass/bandit20`. The first part of the command executes the file,
   and the later part reads the password file only readable by bandit20.

**Password for Level 20:** 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
 
