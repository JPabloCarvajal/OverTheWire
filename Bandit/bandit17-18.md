# Bandit Level 17 → Level 18

### Level Goal
There are 2 files in the homedirectory: `passwords.old` and `passwords.new`. The password for the next level is in `passwords.new` and is the only line that has been changed between `passwords.old` and `passwords.new`

---

### Solution

```bash
vimdiff 'passwords.new' 'passwords.old' # underlined will be the different one we'll use the one in passwords.new
exit
ssh -p 2220 bandit18@bandit.labs.overthewire.org
x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO

ssh bandit18@bandit.labs.overthewire.org -p 2220 # it will log u out (part of the exercise)
```
