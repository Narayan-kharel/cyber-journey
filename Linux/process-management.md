1. Check running processes
ps


Output:

    PID TTY          TIME CMD
   1278 pts/0    00:00:00 bash
   1285 pts/0    00:00:00 ps

ps aux


Output:

USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.1 106592  8624 ?        Ss   10:01   0:01 /sbin/init
kali      1278  0.0  0.2  28036 11000 pts/0    Ss   10:02   0:00 -bash
kali      1320  0.0  0.1  36672  4320 pts/0    R+   10:03   0:00 ps aux

2. Search for a process
ps aux | grep firefox


Output:

kali      1400  5.0  3.0 812345 123456 ?  Sl   10:04   0:20 /usr/lib/firefox/firefox
kali      1432  0.0  0.0  14432   976 pts/0  S+   10:05   0:00 grep firefox

3. Kill a process
kill 1400


Force kill:

kill -9 1400

4. Monitor processes live
top


Output:

top - 10:06:12 up  1:25,  2 users,  load average: 0.15, 0.22, 0.18
Tasks: 225 total,   1 running, 224 sleeping,   0 stopped,   0 zombie
%Cpu(s):  2.1 us,  0.4 sy,  0.0 ni, 97.5 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   7984.0 total,   3200.5 free,   2400.7 used,   2382.8 buff/cache

htop


👉 Easier navigation with arrow keys, press F9 to kill a process.

If missing:

sudo apt install htop

5. Background & Foreground Jobs
sleep 60 &


Output:

[1] 1450

jobs


Output:

[1]+  Running                 sleep 60 &


Bring to foreground:

fg %1


Send back to background:

bg %1