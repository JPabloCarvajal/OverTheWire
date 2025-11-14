# Bandit Level 26 → Level 27

### Level Goal
Good job getting a shell!  
Now hurry and grab the password for **bandit27**.

---

### Solution

```bash
ls -la
./bandit27-do whoami
./bandit27-do cat /etc/bandit_pass/bandit27   # here it is
exit
```

```bash
ssh bandit27@bandit.labs.overthewire.org -p 2220
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
```
