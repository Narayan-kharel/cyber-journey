This one is super important for cybersecurity, since attackers often leave traces in logs, and defenders must know where to look.

📘 Day 14 – Logs & Monitoring
1. System logs location

Most logs are stored in /var/log/:

ls /var/log


Common ones:

/var/log/syslog → General system messages (Debian/Ubuntu)

/var/log/messages → General messages (RedHat/CentOS)

/var/log/auth.log → Authentication attempts

/var/log/dmesg → Kernel/hardware messages

/var/log/apache2/ → Apache web server logs

/var/log/nginx/ → Nginx web server logs

2. View logs
cat /var/log/syslog
tail /var/log/syslog
tail -f /var/log/syslog    # Live updates
less /var/log/auth.log     # Scrollable view

3. Search inside logs
grep "Failed password" /var/log/auth.log
grep "error" /var/log/syslog

4. Journalctl (systemd logs)
journalctl                # Full log
journalctl -u ssh         # Logs for ssh service
journalctl --since "1 hour ago"
journalctl --since "2025-09-01" --until "2025-09-03"

5. Real-time monitoring
dmesg -T                  # Show kernel logs with timestamps
top                       # Real-time process monitoring
htop                      # (install) better process monitor

6. Who is logged in
who
w
last

7. Example Security Check

Check failed SSH logins:

grep "Failed password" /var/log/auth.log | less

📌 Exercises

Use ls /var/log and list the files.

Open /var/log/auth.log and search for "Failed password".

Run journalctl -u ssh --since "10 minutes ago".

Use who and last to check user logins.

Try tail -f /var/log/syslog and open another terminal to run a command, see logs appear in real time.[C[C[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D- [A[A[D[D- use who and last tocheck[A[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[A-run[B[B[B[B[D[try[B[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[A[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[C[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[D[DDay