# Bandit Level5 Solution

**Objective:** Read the human-readable(ASCII), non-executable, 1033 byte sized file named **.file2** inside the folder**maybehere07** inside the **inhere** folder in the home directory.

**Commands Used:**
* `ls`: To list directories and files.
* `cd`: To change into the inhere directory.
* `find`: Was used with `-size` and `-type` to find the right file.
* `cat`: To display the contents of the hidden human-readable **.file2** ASCII file.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit5` with password from level4
2.  Once logged in, use `ls` to see files in the current directory.
3.  You will see a folder named `inhere`.
4.  Use `cd inhere` to access the directory.
5.  Use `ls` to see the files in the current directory.
6.  You will see 17 maybehere* folders. 
6.  Use `find . -type f -size 1033c` to find the file of size 1033 bytes.
7.  You will see the only one file pop up, which is `maybehere07/.file2`.
6.  Use `cat maybehere07/.file2` to print the contents of the file to the screen.

**Password for Level 6:** HWasnPhtq9AVKe0dmk45nxy20cvUa6EG 

