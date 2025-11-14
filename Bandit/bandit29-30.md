# Bandit Level 29 → Level 30

### Level Goal
There is a git repository at:  
`ssh://bandit29-git@bandit.labs.overthewire.org/home/bandit29-git/repo`  
via port **2220**.  
The password for **bandit29-git** is the same as for **bandit29**.

Clone the repository and find the password for the next level.

---

### Solution

```bash
mktemp -d
cd /tmp/tmp.q223bJA0kr

git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo
4pT1t5DENaYuqnqvadYs1oE4QLCdjmJ7   # password for bandit29-git

ls
cd repo

cat README.md
git branch -a
git checkout dev
cat README.md   # here it is
```

```bash
ssh bandit30@bandit.labs.overthewire.org -p 2220
qp30ex3VLz5MDG1n91YowTv4Q8l7CDZL
```
