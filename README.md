# Linux & DevOps Cheatsheet

Beginner-friendly Linux notes, commands, troubleshooting tips, and practical DevOps context.

## Why Linux?

Most servers, cloud virtual machines, containers, and DevOps tools run on Linux. Learning the command line makes it easier to manage systems, investigate problems, and automate work.

## Navigation and Files

| Command | What it does |
| --- | --- |
| `pwd` | Shows your current location. |
| `ls -la` | Lists files and permissions. |
| `cd /path/to/folder` | Moves to a folder. |
| `mkdir project` | Creates a folder. |
| `touch notes.txt` | Creates an empty file. |
| `cp file.txt copy.txt` | Copies a file. |
| `mv old.txt new.txt` | Moves or renames a file. |
| `find . -name "*.log"` | Finds log files. |
| `rm file.txt` | Deletes a file. Use carefully. |

## Viewing and Editing Files

```bash
cat file.txt             # print a small file
less /var/log/syslog     # view a large file; press q to exit
head -n 10 file.txt      # first 10 lines
tail -n 20 file.txt      # last 20 lines
tail -f app.log          # follow a log as it changes
nano file.txt            # simple terminal editor
grep -n "error" app.log  # find error lines
```

## Permissions and Ownership

Linux controls who can read, write, or run files.

```bash
ls -l file.txt           # view permissions and owner
chmod +x script.sh       # allow a script to run
chmod 644 file.txt       # owner can write; others can read
sudo chown user:group file.txt  # change owner and group
```

`sudo` runs a command with administrator privileges. Use it only when needed and double-check commands before pressing Enter.

## Processes and Services

```bash
ps aux                   # list running processes
top                      # live view of CPU and memory use
kill PID                 # ask a process to stop
systemctl status nginx   # check a service
sudo systemctl start nginx
sudo systemctl restart nginx
sudo systemctl enable nginx  # start after reboot
```

## Disk, Memory, and Network Checks

```bash
df -h                    # free disk space
du -sh *                 # folder sizes in current directory
free -h                  # memory usage
uptime                   # uptime and load average
ip addr                  # network addresses
ping -c 4 example.com    # basic connectivity test
curl -I https://example.com  # check an HTTP response
ss -tulpn                # listening ports
```

## Package Management

On Ubuntu and Debian systems:

```bash
sudo apt update
sudo apt install nginx
sudo apt remove nginx
```

On Red Hat, Fedora, and Amazon Linux systems, use `dnf` (or sometimes `yum`) instead of `apt`.

## Logs and Troubleshooting

When something fails, start with the error message and recent logs.

```bash
sudo journalctl -u nginx --since "30 minutes ago"
sudo journalctl -xe
tail -n 50 /var/log/syslog
```

Simple troubleshooting flow:

1. Check the service: `systemctl status service-name`
2. Read its recent logs: `journalctl -u service-name`
3. Check disk and memory: `df -h` and `free -h`
4. Check ports and network access: `ss -tulpn` and `curl`
5. Make one change at a time, then test again.

## Practical Examples

### Find large files

```bash
find /var/log -type f -size +100M 2>/dev/null
```

### Check a website from a server

```bash
curl -s -o /dev/null -w "%{http_code}\n" https://example.com
```

### Securely copy a file to a server

```bash
scp backup.tar.gz user@server.example:/home/user/backups/
```

## Good Habits

- Run `pwd` and `ls` before changing or deleting files.
- Prefer `rm -i file.txt` when learning; it asks for confirmation.
- Keep system updates current, especially on test machines.
- Avoid logging in as `root` for daily work; use a normal user with `sudo`.
- Read logs before restarting services, so useful error information is not lost.
- Store configuration in version control, but never commit passwords or private keys.
- Document changes made to servers and deployment environments.

## DevOps Connection

Linux skills are used every day for cloud servers, Docker containers, CI/CD runners, monitoring, incident response, and application deployments.

> The goal is not to memorise every command—learn how to inspect a system, understand what you see, and make safe changes.
