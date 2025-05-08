# Bandit Level 14 → Level 15

## 🧠 Objective
The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost.
---

## 🧰 Tools & Commands Used
- `nc`

## 🕵️ Walkthrough

```bash
#Step 1: Submit current password to localhost on port 30000 using nc
nc localhost 30000
```
## 📌 Key Takeaways
- Learned about the nc command