1. Check disk space usage
df -h


Example output:

Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1       100G   25G   70G  26% /
tmpfs           2.0G  1.2M  2.0G   1% /run


-h → human-readable (GB/MB instead of blocks).

Shows partitions and how much space is used/available.

2. Check file/folder sizes
du -sh /var/log


Example output:

120M    /var/log


-s → summary (not every file).

-h → human-readable.

👉 Useful for finding which folders eat space.

3. Show top processes by memory/CPU
top


Output (interactive):

PID USER  PR  NI  VIRT  RES  SHR S %CPU %MEM TIME+ COMMAND
1234 root 20   0  400m  50m  10m S  25.0  2.0 0:05 processname


Press q to quit.

%CPU and %MEM show usage per process.

4. Modern alternative to top
htop


(if not installed: sudo apt install htop)

Easier to read, color-coded, shows graphs.

5. Disk usage per file/folder (sorted)
du -ah /var | sort -rh | head -n 10


Shows largest 10 files/folders in /var.

6. Check free RAM
free -h


Example output:

              total        used        free      shared  buff/cache   available
Mem:           8.0G        2.5G        3.0G        200M        2.5G        5.0G
Swap:          2.0G          0B        2.0G
