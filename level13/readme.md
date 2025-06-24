# Bandit Level13 Solution

**Objective:** Find the password by logging in as bandit14 using the ssh private key.

**Commands Used:**
* `ls`: To list directories and files.
* `cat`: To feed the contents of data.txt into tr.
* `ssh`: To log in using the private key.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit13` with password from level12
2.  Once logged in, use `ls` to see the contents.
3.  You will see a file named `sshkey.private`.
4.  Use `ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220` to log in as bandit14.
5.  Once logged in, use `cat /etc/bandit_pass/bandit14` to see the password.

**Password for Level 14:** MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS

