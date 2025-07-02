# Bandit Level20 Solution

**Objective:** To set up a server that echoes the current password and execute the setuid in home directory.

**Commands Used:**
* `echo`: To echo the password.
* `nc`: To set up a server on locahost with a specific port.

**Steps:**
1.  Use `ssh bandit20@bandit.labs.overthewire.org -p 2220` to login as user `bandit20`.
2.  Use `ls -l`, you will see a setuid binary file that is set up to connect to a server on a specific port and expects the current 
   level password.
3.  Open a separate window and type `echo "PASSWORD" | nc -l -p XXXXX`. This will create a daemon listening on port XXXXX and waiting
   to ehco the current password.
4.  Go back to the previous window and type `/home/bandit20/suconnect XXXXX`. This will execute the setuid and connect to port XXXXX
   and send back the password.

**Password for Level 21:** EeoULMCra2q0dSkYj561DX7s1CpBuOBt
