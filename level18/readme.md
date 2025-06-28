# Bandit Level18 Solution

**Objective:** Log in bypassing the .bashrc and read the readme to obtain the password.

**Commands Used:**
* `bash`: To bypass malicious .bashrc.

**Steps:**
1.  Use `ssh bandit18@bandit.labs.overthewire.org -p 2220 "bash --norc` to login as user `bandit18` and bypass .bashrc.
2.  Enter the password. You will be logged in, although no such confirmation will be seen.
3.  Once logged in, use `ls` to find the readme.
4.  Use `cat readme` to obtain the password.

**Password for Level 19:** cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8
