# Bandit Level 17 → Level 18

## 🧠 Objective
There are 2 files in the homedirectory: passwords.old and passwords.new. The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new
---

## 🧰 Tools & Commands Used
- `diff`

## 🕵️ Walkthrough

```bash
# Step 1: Compare both files using diff
diff passwords.old passwords.new
```
## 📌 Key Takeaways
- Learned about the diff command for the first time and implemented it
