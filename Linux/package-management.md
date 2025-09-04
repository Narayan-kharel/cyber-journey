1. Update package list
sudo apt update


Updates the list of available packages from repositories.

Run this before installing anything.

2. Upgrade installed packages
sudo apt upgrade


Installs the latest versions of all packages currently installed.

3. Install a package
sudo apt install nmap


Installs the nmap tool.

Replace nmap with any package name.

4. Remove a package
sudo apt remove nmap


Removes package but leaves config files.

👉 Remove with config files:

sudo apt purge nmap

5. Search for a package
apt search wireshark

6. Show package details
apt show nmap

7. Work with .deb files (using dpkg)

Download package first (example):

wget http://ftp.us.debian.org/debian/pool/main/n/nmap/nmap_7.80-1_amd64.deb


Install it manually:

sudo dpkg -i nmap_7.80-1_amd64.deb


Fix dependencies if needed:

sudo apt --fix-broken install

8. List installed packages
dpkg -l | less

9. Check if a package is installed
dpkg -l | grep nmap