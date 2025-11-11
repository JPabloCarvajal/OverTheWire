# Bandit Level 1 → Level 2

### Level Goal
The password for the next level is stored in a file called - located in the home directory

---

### Solution

```bash
cat ./-  # to read a file named "-"
exit
ssh -p 2220 bandit2@bandit.labs.overthewire.org
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```