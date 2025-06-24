# Bandit Level12 Solution

**Objective:** Decode the data in the data.txt file located in home directory.

**Commands Used:**
* `mktemp`: To make a temporary directory to work in.
* `cp`: To copy the data.txt file from the working directory to the temporary one.
* `cd`: To access the temporary directory.
* `ls`: To list directories and files.
* `xxd`: To convert files to binary data from hexdump.
* `file`: To identify the file type fo different compressed files.
* `zcat`: To unzip gzip compressed data.
* `tar`: To unzip POSIX tar archive files.
* `bzcat`: To unzip bzip2 compressed data.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit12` with password from level11
2.  Once logged in, use `ls` to see the contents.1
3.  You will see a file named `data.txt`.
4.  Use `mktemp -d` to create a temporary directory in the /tmp/ folder.
5.  Use `cp data.txt /tmp/tmp.XXXXXXXX` to copy the file into the temporary directory.
6.  Use `cd /tmp/tmp.XXXXXXXX` to access that directory.
7.  Use `xxd -r data.txt hex_rev` to convert the hexdump into binary and write the output to a file named `hexrev`.
8.  Use `file hex_rev` to identify the file type, you'll see it's a gzip compressed file.
9.  Use `zcat hex_rev >> uncomp1` to unzip and write the new file to uncomp1.
10. Use `file` again to check the file size of uncomp1, you'll see that it's bzip2 compressed data.
11. Use `bzcat uncomp1 >> uncomp2` to unzip the bzip2 data and write the new file into uncomp2.
12. Find uncomp2 to be a gzip file, unzipping it using `zcat uncomp2 >> uncomp3` and testing the file shows POSIX tar archive.
13. Use `tar -xvf uncomp3`, which unzips the file and writes it in **data5.bin** which is printed in the standard output.
14. Use `file data5.bin` to see that it's also a POSIX tar archive, so repeat the process using `tar -xvf data5.bin`.
15. This will create **data6.bin** which upon testing with `file data6.bin` reveals itself to be a bzip2 compressed data.
16. Use `bzcat data6.bin >> uncomp4` then use `file uncomp4` to see that its another POSIX tar archive.
17. Use `tar -xvf uncomp4` to unzip it. This will create a **data8.bin file**, which is a gzip compressed data.
18. Finally, use `zcat data8.bin` to obtain the password.

**Password for Level 13:** FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn

