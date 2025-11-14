# Bandit Level 28 → Level 29

### Level Goal
There is a git repository at:  
`ssh://bandit28-git@bandit.labs.overthewire.org/home/bandit28-git/repo`  
via port **2220**.  
The password for **bandit28-git** is the same as for **bandit28**.

Clone the repository and find the password for the next level.

---

### Solution

```bash
exit   # if you are still logged into bandit28

mktemp -d
cd /tmp/tmp.q223bJA0kr
git clone ssh://bandit28-git@bandit.labs.overthewire.org:2220/home/bandit28-git/repo
cd repo

git log
git show b0354c7be30f500854c5fc971c57e9cbe632fef6   # here it is
```

```bash
ssh bandit29@bandit.labs.overthewire.org -p 2220
4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7
```
