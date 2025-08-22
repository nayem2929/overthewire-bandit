# Bandit Level22 Solution

**Objective:** A program is running automatically at regular intervals from cron, the time-based job scheduler. Look 
in /etc/cron.d/ for the configuration and see what command is being executed.

**Commands Used:**
* `cd`: To change directories.
* `cat`: To read files.
* `md5sum`: To obtain the appropriate file name.

**Steps:**
1.  Use `ssh bandit22@bandit.labs.overthewire.org -p 2220` to login.
2.  Use `cd /etc/cron.d/` to change into the directory where the cronjob is located.
3.  Use `cat cronjob_bandit23` to see the output as such:
  @reboot bandit23 /usr/bin/cronjob_bandit23.sh &> /dev/null
  * * * * * bandit23 /usr/bin/cronjob_bandit23.sh &> /dev/null
   The stars indicate that this is a job repeating every minute of every hour and it's running a shell script. The shell
   script is being run once at reboot and then repearting every minute. It's also discarding the standard output and 
   error messages by redirecting them to /dev/null. This script is being executed by user `bandit23`.
5.  Use `cat /usr/bin/cronjob_bandit22.sh` to read the file. The output will be as such:
  #!/bin/bash
  myname=$(whoami)
  mytarget=$(echo I am user $myname | md5sum | cut -d ' ' -f 1)
  echo "Copying passwordfile /etc/bandit_pass/$myname to /tmp/$mytarget"
  cat /etc/bandit_pass/$myname > /tmp/$mytarget
  This script takes in the user that is executing the script and writing the password to a file whose name is generated using the
  md5sum hash.
6.  Use `echo I am user bandit23 | md5sum | cut -d ' ' -f 1` to obtain the filename that has the password for level 23.
6.  Reading this file using `cat /tmp/8ca319486bfbbc3663ea0fbe81326349` gives the password to the next round.

**Password for Level 23:** 0Zf11ioIjMVN551jX3CmStKLYqjk54Ga
