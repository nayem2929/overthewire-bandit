# Bandit Level6 Solution

**Objective:** Find the 33 byte, owned by user bandit7, owned by group bandit6 file stored somewhere on the server.

**Commands Used:**
* `ls`: To list directories and files.
* `cd`: To change into the inhere directory.
* `find`: Was used with `-size` and `-type` to find the right file.
* `cat`: To display the contents of the hidden human-readable **.file2** ASCII file.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit6` with password from level5
2.  Once logged in, use `cd ..` to access home directory.
3.  Use `cd ..` again to access the root(/) directory.
4.  Use `find -type f -user bandit7 -group bandit6 2>/dev/null`
5.  You will see the following path pop up: `./var/lib/dpkg/info/bandit7.password`
6.  Use `cd var/lib/dpkg/info` and then `cat bandit7.password`.
7.  Use `ls -l badit7.password` to verify the 33 byte file size.

**Password for Level 7:** morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj

