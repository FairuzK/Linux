# Bandit Solutions
The OverTheWire Bandit exercises are a series of online challenges designed to teach basic Linux command-line skills. Below are solutions to the different levels.

Level 0 starts by testing how to use the ssh command and has no flag or password, only requires using the syntax below.
```bash
ssh -p 2220 bandit.labs.overthewire.org -l bandit0
 ```

## Bandit Level 1 - 2
### Commands Used

```bash
ls
ls -lah
cat readme
```
### Lessons
-  Listing of files
-  Reading files
---

## Bandit Level 2 - 3
### Commands Used
```bash
ls
cat   cat --spaces\ in\ this\ filename--
```
### Lessons
- Learning how to work with spaces in the file, i.e., "\\"
---

## Bandit Level 3-4
### Commands Used
```bash
ls
cd inhere
ls -a
cat ...Hiding-From-You
```
### Lessons
- How to find and read Hidden files.
---


## Bandit Level 4-5
### Commands Used
``` bash
ls
cd inhere
ls
file ./*
cat ./-file07
```
### Lessons
- Identify and read file types 
---


## Bandit Level 5-6
### Commands Used
``` bash
ls
cd inhere
find . -type f -size 1033c ! excutable
cat ./maybehere/.file2
```
### Lessons
- How to find and search files with specific requirements
---


## Bandit Level 6-7
### Commands Used
```bash
find / -type f user bandit7 -group bandit6 -size 33c 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
```
### Lessons
- How to search while ignoring permission errors
---


## Bandit Level 7-8
### Commands used
```bash
ls
grep "millionth" data.txt
```
### Lessons
- How you can search inside a text file using the grep command.
---


## Bandit Level 8-9
### Commands Used
```bash
ls
sort data.txt | uniq -u
```
### Lessons
- Learn how to sort and find Unique Data
---


## Bandit Level 9-10
### Commands Used
```bash
ls
strings data.txt | grep "="
```
### Lessons
- Learn how to extract readable text from binary files
---


## Bandit Level 10-11
### Commands Used
```bash
ls
base64 -d data.xt
```
### Lessons
- Learn how to decode base64-encoded data from a file
---


## Bandit Level 11-12
### Commands Used
```bash
ls
cat data.txt | tr 'A-ZA-z' 'N-ZA-Mn-za-m'
```
### Lessons
- Learn how to translate characters in a file using the tr command.
--- 


## Bandit Level 12-13
### Commands Used
```bash
mkdir /tmp/bandit
cp data.txt /tmp/bandit
cd /tmp/bandit
xxd -r data.txt > data
file data
gzip -d data.gz
bzip2 -d data.bz2
tar -xf data.tar
```
### Lessons
- Learn how to extract and decompose different archive formats
---

## Bandit Level 13-14
### Commands Used
```bash
ls
ssh -i sshkey.private bandit14@localhost -p 2220
```
### Lessons
- Learn how to log in using an SSH private key
---

## Bandit Level 14-15
### Commands Used
```bash
cat /etc/bandit_pass/bandit14
nc localhost 30000
```
### Lessons
- Learn how to connect to a service using Netcat.
---

## Bandit Level 15-16
### Commands Used
```bash
openssl  s_client -connect localhost:30001
```
### Lessons
- Learn how to establish a secure SSL/TLS connection.
---

## Bandit Level 16-17
### Commands Used
```bash
nmap localhost
openssl s_client -connect localhost:31790
```
### Lessons
- Learn how to scan ports and identify the correct device.
---

## Bandit Level 17-18
### Commands Used
```bash
diff passwords.old passwords.new
```
### Lessons
- Learn how to compare two files using the diff command
---

## Bandit Level 18-19
### Commands Used
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme"
```
### Lessons
- Learn how to execute a command during an SSH connection.
---

## Bandit Level 19-20
### Commands Used
```bash
ls
./bandit20-do cat /etc/bandit_pass/bandit20
```
### Lessons
- Learn how to run a command with another permission..
---

