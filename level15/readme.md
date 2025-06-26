# Bandit Level15 Solution

**Objective:** Submit the password of the current level over an encrypted connnection.

**Commands Used:**
* `echo`: To pass on the password to **openssl**.
* `openssl`: To send data over a secure connection.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit15` with password from level14.
2.  Once logged in, use `echo "PASSWORD" | openssl s_client localhost:30001` to obtain the password.

**Password for Level 16:** kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx

