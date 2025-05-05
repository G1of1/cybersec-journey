# Bandit Level 20 → Level 21

## 🧠 Objective
There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).
---

## 🧰 Tools & Commands Used
- `nc`
- `./suconnect`
- `ls`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit20@bandit.labs.overthewire.org -p 2220

#Step 2: Use ls command to find the needed setuid binary
ls

# Step 3: Split the terminal to run nc on a seperate instance


#Step 3: Run nc to listen to the connection on port 2222
nc -lvp 2222

# Step 4: On the other terminal run the setuid binary
./suconnect

#Step 5: Use the password from the current level while listening to get the password to the next level

