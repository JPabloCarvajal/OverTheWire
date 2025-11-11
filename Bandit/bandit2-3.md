# Bandit Level 2 → Level 3

### Level Goal
The password for the next level is stored in a file called --spaces in this filename-- located in the home directory

---

### Solution

```bash
ls -la
cat './--spaces in this filename--'   # to read a file with spaces use './file name'
# here is the psswd
exit
ssh -p 2220 bandit3@bandit.labs.overthewire.org
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx
```