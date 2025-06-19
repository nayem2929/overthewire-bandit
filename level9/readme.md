# Bandit Level9 Solution

**Objective:** The password is one of the few human readable strings next to a bunch of '=' signs in the data.txt file located in home directory.

**Commands Used:**
* `ls`: To list directories and files.
* `strings`: To filter out the binary and other non-readable lines.
* `grep`: To identify the line that's adjacent to a bunch of '=' signs.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit9` with password from level8
2.  Once logged in, use `ls` to see the contents.
3.  You will see a file named `data.txt`.
4.  Use `strings data.txt | grep "==="`.
5.  The password will show up in the 4th line.

**Password for Level 9:** FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey

