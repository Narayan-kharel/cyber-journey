1. Viewing File Permissions
ls -l


👉 Shows file details, including permissions.

Example output:

-rw-r--r--  1 user user   123 Sep  2  notes.txt
drwxr-xr-x  2 user user  4096 Sep  2  scripts/


Breakdown of -rw-r--r--:

- → regular file (d would mean directory)

rw- → owner can read & write

r-- → group can only read

r-- → others can only read

2. Changing Permissions with chmod

Add execute permission for user:

chmod u+x script.sh


Remove read permission for group:

chmod g-r file.txt


Set read, write, execute for everyone:

chmod 777 file.txt

3. Numeric Permissions

Each permission has a value:

r = 4

w = 2

x = 1

So:

chmod 644 file.txt → owner=read/write, group=read, others=read

chmod 755 script.sh → owner=all, group=read+execute, others=read+execute

4. Changing Ownership

Change owner:

sudo chown newuser file.txt


Change group:

sudo chgrp devs file.txt


Change both owner & group:

sudo chown newuser:newgroup file.txt

5. Special Permissions (advanced but important)

Setuid (4xxx) → runs file as owner.

Setgid (2xxx) → new files inherit group.

Sticky bit (1xxx) → only owner can delete files inside a folder.

Example:

chmod 4755 program