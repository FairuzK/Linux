### Search with grep
```bash
grep "error" /var/log/syslog
grep -r "TODO" ~/projects/
```
### Advanced grep
```bash
grep -i "failed" /var/log/auth.log | wc -l  # count failed login attempts
```
### awk examples
```bash
ps aux | awk '{print $1, $11}'  # print user and command
cat /etc/passwd | awk -F: '{print $1, $6}'  # print username and home dir
```
### sed examples
```bash
sed 's/old/new/g' file.txt  # replace text
sed -n '10,20p' file.txt    # print lines 10-20
```
### Piping chains
```bash
cat /var/log/syslog | grep "error" | awk '{print $1, $2, $3}' | sort | uniq
```