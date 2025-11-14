# Bandit Level 27 → Level 28

### Level Goal
There is a git repository at:  
`ssh://bandit27-git@bandit.labs.overthewire.org/home/bandit27-git/repo`  
via port **2220**.  
The password for **bandit27-git** is the same as for **bandit27**.

Clone the repository and find the password for the next level.

---

### Solution

```bash
# log out of bandit27 if you're still inside
exit

mkdir /tmp/foldername
git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo
cd repo
cat README    # here it is
```

```bash
ssh bandit28@bandit.labs.overthewire.org -p 2220
Yz9IpL0sBcCeuG7m9uQFt8ZNpS4HZRcN
```
