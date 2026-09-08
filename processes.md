##Learn to monitor and manage processes:
### View processes
```bash
ps aux
ps aux | grep nginx
```

### Real-time monitoring
```bash
top
htop  # install via: sudo apt install htop
```

### Background processes
```bash
sleep 100 &
jobs
fg %1  # bring to foreground
bg %1  # send to background
```

### Kill processes
```bash
kill <PID>
killall sleep
```