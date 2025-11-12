# Bandit Level 13 → Level 14

### Level Goal
The password for the next level is stored in `/etc/bandit_pass/bandit14` and can only be read by user `bandit14`. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. Note: `localhost` is a hostname that refers to the machine you are working on

---

### Solution

```bash
ls 
cat sshkey.private    # copy
exit
nano sshkey.private   # copy the key
chmod 600 sshkey.private 
ssh -i sshkey.private -p 2220 bandit14@bandit.labs.overthewire.org
cat /etc/bandit_pass/bandit14 # here it is
exit
ssh -p 2220 bandit14@bandit.labs.overthewire.org
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
```
