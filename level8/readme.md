# Bandit Level8 Solution

**Objective:** Find the password in the line that only occurs once in the data.txt file located in home directory.

**Commands Used:**
* `ls`: To list directories and files.
* `sort`: To sort the files and prepare it for `uniq`.
* `uniq`: To identify the line that's appears only once in the file.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit8` with password from level7
2.  Once logged in, use `ls` to see the contents.
3.  You will see a file named `data.txt`.
4.  Use `sort data.txt | uniq -u`.
5.  The `-u` option allows `uniq` to print out the lines that appear only once in the file.

**Password for Level 9:** 4CKMh1JI91bUIZZPXDqGanal4xvAg0JM

