1. Create a new user
sudo adduser alice


Creates user alice, sets password, creates /home/alice/.

2. Add a user to a group
sudo usermod -aG sudo alice


-aG → append to group.

This makes alice a sudoer (can run admin commands).

3. Check group memberships
groups alice


Output:

alice : alice sudo

4. Create a new group
sudo groupadd developers


Then add a user:

sudo usermod -aG developers alice

5. Switch users
su - alice


Switch to alice’s shell (the - loads their environment).

👉 Return to your user:

exit

6. Sudo privileges test
sudo whoami


Output:

root


Confirms the user has sudo access.

7. Remove a user from a group
sudo gpasswd -d alice developers

8. Delete a user
sudo deluser alice


Delete with home folder too:

sudo deluser --remove-home alice