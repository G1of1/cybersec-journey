# Bandit Level 13 → Level 14

## 🧠 Objective
The password for the next level is stored in /etc/bandit_pass/bandit14 and can only be read by user bandit14. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: localhost is a hostname that refers to the machine you are working on
---

## 🧰 Tools & Commands Used
- `ssh`
-  `ls`, `cat`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH
ssh bandit13@bandit.labs.overthewire.org -p 2220

# Step 2: Find the SSH Key
ls

#Step 3: Connect to bandit14
ssh bandit14@localhost -p 2220 -i sshkey.private

#Step 4: Print the password
cat /etc/bandit_pass/bandit14
```

## 📌 Key Takeaways
- Learned about private ssh keys and how they are used to establish connections
