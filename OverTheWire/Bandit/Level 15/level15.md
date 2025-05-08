# Bandit Level 15 → Level 16

## 🧠 Objective
The password for the next level can be retrieved by submitting the password of the current level to port 30001 on localhost using SSL/TLS encryption.
---

## 🧰 Tools & Commands Used
- `ssh`
-  `openssl`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit15@bandit.labs.overthewire.org -p 2220

# Step 2: Connect to localhost on port 30001 via OpenSSL
openssl -s_client -connect localhost:30001

#Step 3: Paste the password to beat the level
```
## 📌 Key Takeaways
- Learned about openssl and some its use cases