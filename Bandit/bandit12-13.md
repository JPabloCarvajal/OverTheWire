# Bandit Level 12 → Level 13

### Level Goal
The password for the next level is stored in the file `data.txt`, which is a hexdump of a file that has been repeatedly compressed.  
For this level it may be useful to create a directory under `/tmp` in which you can work. Use `mkdir` with a hard to guess directory name. Or better, use the command `mktemp -d`. Then copy the datafile using `cp`, and rename it using `mv` (read the manpages!)

---

### Solution

```bash
cd /tmp 
mkdir changethisname
cd changethisname
cp ~/data.txt ./

# we are going to revert the hexdump and get the real data
xxd -r data.txt realdata
ls
cat realdata

# to see which type of decompresion are we using we have to see the first bytes of the data
cat data.txt
xxd data.txt 

# GZIP \x1F\x8B\x08
mv realdata.txt compressed_data.gz
gzip -d compressed_data.gz

# BZIP2 425a means bzip and 68 means version 2 then we´ll use bzip2
xxd compressed_data 
mv compressed_data compressed_data.bz2

# GZIP \x1F\x8B\x08
xxd compressed_data 
mv compressed_data compressed_data.gz
gzip -d compressed_data.gz

# TAR data5.bixx at the end of the line
xxd compressed_data 
mv compressed_data compressed_data.tar
tar -xf compressed_data.tar
tar -xf data5.bin
ls
xxd data6.bin

# bzip2 again (425a 68)
bzip2 -d data6.bin
ls 
tar -xf data6.bin.out
ls
xxd data8.bin

#  1f8b 0808  GZIP AGAIN!!!
mv data8.bin godpleasebethisisthelastone.gz
gzip -d godpleasethisisthelastone.gz
ls
cat godpleasethisisthelastone # here it is
exit
ssh -p 2220 bandit13@bandit.labs.overthewire.org
FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```
