# Bandit Level16 Solution

**Objective:** Submit the password of the current level into the right port to obtain the credentials for the next level.

**Commands Used:**
* `nmap`: To scan the ports.
* `ncat`: To find the right port.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit16` with password from level15.
2.  Once logged in, use `nmap -p 31000-32000 localhost` to find the ports that are open and listening.
3.  You will see 5 ports. Now, use `ncat --ssl localhost XXXXX` to check if a port is using SSL/TLS.
4.  If a connection is established, enter the current level's password.
4.  The 1st and the 3rd port will return an error, and the 2nd port will echo back the password. The 4th port will
   send back an RSA key for the next level. 

**Password for Level 17:** [bandit17_key](level16/bandit17_key)
 

