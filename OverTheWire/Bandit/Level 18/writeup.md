# Bandit Level 18 → Level 19

## 🧠 Objective
The password for the next level is stored in a file readme in the homedirectory. Unfortunately, someone has modified .bashrc to log you out when you log in with SSH.
---

## 🧰 Tools & Commands Used
- `cat`

## 🕵️ Walkthrough

```bash
# Step 1: Connect via SSH and at the same time write the command cat so that it will print the file before the connection closes.
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```
## 📌 Key Takeaways
- Learned about how shells can be implemented to attack users.