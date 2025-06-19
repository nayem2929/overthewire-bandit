# Bandit Level10 Solution

**Objective:** Decode the base64 encoded data.txt file located in home directory.

**Commands Used:**
* `ls`: To list directories and files.
* `decode`: To decode base64 encoded data.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit10` with password from level9
2.  Once logged in, use `ls` to see the contents.
3.  You will see a file named `data.txt`.
4.  Use `base64 -d data.txt`.
5.  The password will show up in the 1st line.

**Password for Level 10:** dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

