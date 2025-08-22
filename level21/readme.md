# Bandit Level21 Solution

**Objective:** A program is running automatically at regular intervals from cron, the time-based job scheduler. Look 
in /etc/cron.d/ for the configuration and see what command is being executed.

**Commands Used:**
* `cd`: To change directories.
* `cat`: To read files.

**Steps:**
1.  Use `ssh bandit21@bandit.labs.overthewire.org -p 2220` to login.
2.  Use `cd /etc/cron.d/` to change into the directory where the cronjob is located.
3.  Use `cat cronjob_bandit22` to see the output as such:
  @reboot bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
  * * * * * bandit22 /usr/bin/cronjob_bandit22.sh &> /dev/null
   The stars indicate that this is a job repeating every minute of every hour and it's running a shell script. The shell
   script is being run once at reboot and then repearting every minute. It's also discarding the standard output and 
   error messages by redirecting them to /dev/null. This script is being executed by user `bandit22`.
5.  Use `cat /usr/bin/cronjob_bandit22.sh` to read the file. The output will be as such:
  #!/bin/bash
  chmod 644 /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
  cat /etc/bandit_pass/bandit22 > /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv
  The first line tells the operating system to run the following commands in the second and third line using the bash 
  interpreter. The second line is changing permissions to a temp file, where the password is later written.
6.  Reading this file using `cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv` gives the password to the next round.

**Password for Level 22:** tRae0UfB9v0UzbCdn9cY0gQnds9GF58Q
