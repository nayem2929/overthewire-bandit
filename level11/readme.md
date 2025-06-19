# Bandit Level11 Solution

**Objective:** Decode the data using ROT13 encryption in the data.txt file located in home directory.

**Commands Used:**
* `ls`: To list directories and files.
* `cat`: To feed the contents of data.txt into tr.
* `tr`: To perform ROT13 decryption.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit11` with password from level10
2.  Once logged in, use `ls` to see the contents.
3.  You will see a file named `data.txt`.
4.  Use `cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'` to perform the ROT13 decryption.
5.  The password will show up in the 1st line.

**Password for Level 12:** 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

