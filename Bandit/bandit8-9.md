# Bandit Level 8 → Level 9

### Level Goal
The password for the next level is stored in the file data.txt and is the only line of text that occurs only once

---

### Solution

```bash
ls
#sort: This command takes the output from cat and sorts the lines alphabetically. Sorting is #crucial for uniq to work correctly, as uniq only detects consecutive duplicate lines.

#uniq -u: This command takes the sorted output and prints only the unique lines, meaning #lines that appear only once in the sorted input. The -u option specifically instructs uniq #to only output lines that are not repeated.

cat data.txt | sort | uniq -u # here it is

exit
ssh -p 2220 bandit9@bandit.labs.overthewire.org
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
```

