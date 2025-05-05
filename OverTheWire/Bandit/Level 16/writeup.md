# Bandit Level 16 → Level 17

## 🧠 Objective
The credentials for the next level can be retrieved by submitting the password of the current level to a port on localhost in the range 31000 to 32000. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.
---

## 🧰 Tools & Commands Used
- `ssh`
- `openssl`
- `nano`
- `mkdir`
- `chmod`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit16@bandit.labs.overthewire.org -p 2220

# Step 2: Use nmap to scan the port range using localhost
nmap localhost -p 31000-32000

#Step 3: Using the open ports given by nmap scan those ports to determine the service versions running on them

nmap localhost -p, 31046, 31518, 31691, 31790, 31960 -sV -T4

#Step 4: Use openssl to setup a connection with localhost using the SSL ports that are open
openssl s_client -connect localhost:<port>

#Step 5: Copy private key and create a new file for the private rsa key on the bandit16
cd /tmp
mkdir lebron
cd lebron
nano rsafile

#Step 6: Set rsafile permission to only allow the owner to read and write
chmod 600 rsafile

#Step 7: Use the rsa key to enter bandit17

ssh -i rsafile bandit17@localhost -p 2220
