# Bandit Level 0 → Level 1

### Level Goal
The password for the next level is stored in a file called readme located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

---

### Solution

```bash
ls -l
cat readme
exit
ssh -p 2220 bandit1@bandit.labs.overthewire.org
ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
```