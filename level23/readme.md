# Bandit Level23 Solution

**Objective:** A program is running automatically at regular intervals from cron, the time-based job scheduler. Look in /etc/cron.d/ for the configuration and see what command is being executed.

**Commands Used:**
   `cd`, `cat`, `chmod`, `nano`

**Steps:**
1.  Use `ssh bandit23@bandit.labs.overthewire.org -p 2220` to login.
2.  Use `cd /etc/cron.d/` to change into the directory where the cronjob is located.
3.  Use `cat cronjob_bandit24` to see the output as such:
  @reboot bandit23 /usr/bin/cr@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
  * * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
   The stars indicate that this is a job repeating every minute of every hour and it's running a shell script. The shell script is being run once at reboot and then repearting every minute. It's also discarding the standard output and error messages by redirecting them to /dev/null. This script is being executed by user `bandit24`.
5.  Use `cat /usr/bin/cronjob_bandit24.sh` to read the script. The output will be written in a separate file. But upon observation, we see that the script is going through scripts in a specific folder, looking for the script with bandit23 as the owner, executing the script if found, then deleting eveything except the hidden folders. 
6.  To write the shell script that will get us our password, we then create a folder inside `/tmp/` and create two files there. One of them is a script that will be copied to the designated folder to be executed as `bandit24`. The other one will be a text file which will be used to copy the password into. The script is very simple:
  `#! /bin/bash`
  `cat /etc/bandit_pass/bandit24 > tmp/myfolder/bandit24_pass`
  This script takes advantage of being run by the user `bandit24` in order to obtain the password.
7.  An important step here now is to change permissions using chmod. We use `chmod o+w /tmp/myfolder/bandit24_pass` to allow the user bandit24 to write into out text file for the password.
8.  Then we copy the script using `cat myscript.sh > /var/spool/bandit24/foo/myscript.sh` and use `chmod o+x /var/spool/bandit24/foo` to allow the user bandit24 to execute the script.
9.  Finally we wait until the next minute so the script executes.
6.  After this, reading this file using `cat /tmp/myfolder/bandit24_pass` gives the password to the next round.

**Password for Level 24:** gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8 
