# Day 4 — File Permissions

**Commands practiced:**
```bash
ls -l script.sh
chmod o-x script.sh
chmod g+w script.sh
ls -l script.sh


Output before chmod:
-rwxr--r-- 1 user user 28 Aug 31 10:15 script.sh

Output after chmod:
-rwxrw-r-- 1 user user 28 Aug 31 10:20 script.sh

Notes:

Owner has read, write, execute

Group has read, write

Others have read