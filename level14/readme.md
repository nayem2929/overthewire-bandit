# Bandit Level14 Solution

**Objective:** Submit the password of the current level on a specific port on localhost.

**Commands Used:**
* `echo`: To pass on the password to **nc**.
* `nc`: To send a file to the server.

**Steps:**
1.  SSH into `bandit.labs.overthewire.org` as user `bandit14` with password from level13
2.  Once logged in, use `echo PASSWORD | nc localhost 30000` to obtain the password.

**Password for Level 15:** 8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo

