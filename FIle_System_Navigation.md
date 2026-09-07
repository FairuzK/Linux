### Navigation
``` bash
cd /var/log
ls -lah
pwd

```

### File operations
```bash
touch test.txt
mkdir -p projects/demo
cp test.txt projects/demo/
mv projects/demo/test.txt projects/demo/backup.txt
rm projects/demo/backup.txt
```

### Viewing files
```bash
cat /etc/passwd
less /var/log/syslog
head -n 20 /etc/services
tail -f /var/log/auth.log
```