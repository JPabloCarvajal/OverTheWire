# Bandit Level 9 → Level 10

### Level Goal
The password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several `=` characters.

---

### Solution

```bash
grep -a === data.txt # here it is
exit
ssh -p 2220 bandit10@bandit.labs.overthewire.org
FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
