# Bandit Level 3 → Level 4

### Level Goal
The password for the next level is stored in a hidden file in the `inhere` directory.

---

### Solution

```bash
ls -la
cd inhere
cat './...Hiding-From-You'   # same from last level use './file name'
exit
ssh -p 2220 bandit4@bandit.labs.overthewire.org
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
```
