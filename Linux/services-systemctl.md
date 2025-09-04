. Check service status
systemctl status ssh


Output:

● ssh.service - OpenBSD Secure Shell server
   Loaded: loaded (/lib/systemd/system/ssh.service; enabled)
   Active: active (running) since Tue 2025-09-02 10:00:00 AEST


Shows if the service is running, enabled, and logs.

2. Start / Stop / Restart a service
sudo systemctl start ssh
sudo systemctl stop ssh
sudo systemctl restart ssh

3. Enable / Disable service at boot
sudo systemctl enable ssh
sudo systemctl disable ssh

4. List all services
systemctl list-units --type=service

5. Check if a service is enabled
systemctl is-enabled ssh

6. Reload service without restarting
sudo systemctl reload ssh


Applies new config changes without full restart (if supported).

7. Example with Apache2 (web server)
sudo apt install apache2 -y
sudo systemctl status apache2


Then visit http://localhost to test.

8. Journal logs for a service
journalctl -u ssh


Shows logs specifically for ssh.