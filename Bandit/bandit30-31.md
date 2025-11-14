# Bandit Level 30 → Level 31

### Level Goal
There is a git repository at:  
`ssh://bandit30-git@bandit.labs.overthewire.org/home/bandit30-git/repo`  
via port **2220**.  
The password for **bandit30-git** is the same as for **bandit30**.

Clone the repository and find the password for the next level.

---

### Solution

```bash
mktemp -d
cd /tmp/tmp.1pxIgKXggQ

git clone ssh://bandit30-git@bandit.labs.overthewire.org:2220/home/bandit30-git/repo
qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL   # password when prompted

cd repo
ls -la
cat README.md
git tag
git show secret   # here it is
```

```bash
ssh bandit31@bandit.labs.overthewire.org -p 2220
fb5S2xb7bRyFmAvQYQGEqsbhVyJqhnDy
```
