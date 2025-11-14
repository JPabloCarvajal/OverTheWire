# Bandit Level 31 → Level 32

### Level Goal
There is a git repository at:  
`ssh://bandit31-git@bandit.labs.overthewire.org/home/bandit31-git/repo`  
via port **2220**.  
The password for **bandit31-git** is the same as for **bandit31**.

Clone the repository and find the password for the next level.

---

### Solution

```bash
mktemp -d
cd /tmp/tmp.LZZUmLNsSR

git clone ssh://bandit31-git@bandit.labs.overthewire.org:2220/home/bandit31-git/repo
fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy

cat README.md
nano key.txt     # write: May I come in?

git add -f key.txt
git commit -m "Access request"
git push
```

```bash
ssh bandit32@bandit.labs.overthewire.org -p 2220
3O9RfhqyAlVBEZpVb6LYStshZoqoSx5K
```
