Script and manage permissions using an example of hello.sh file
### Create a script
```bash
echo '#!/bin/bash\necho "Hello DevOps"' > hello.sh
```

### Make it executable
```bash
chmod +x hello.sh
```

### Run it
```bash
./hello.sh
```

### Change ownership
```bash
sudo chown root:root hello.sh
```
### Understanding permissions
```bash
ls -l hello.sh
```
# Output: -rwxr-xr-x 1 root root 32 Nov 29 10:00 hello.sh
# Breakdown: owner(rwx) group(r-x) others(r-x)