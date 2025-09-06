This is 🔑 for cybersecurity because networking = attack surface. If you master these, you’ll be more confident in SOC, pentesting, or blue-team roles.

📘 Day 15 – Networking Basics
1. Check connectivity
ping google.com
ping -c 4 8.8.8.8        # Only send 4 packets

2. View network interfaces
ip a
ifconfig      # (older, may need `net-tools` package)

3. Routing table
ip route
route -n       # older command

4. Open ports & connections
netstat -tuln      # Show TCP/UDP listening ports
netstat -tnp       # Show programs using ports
ss -tuln           # Modern replacement for netstat
lsof -i :22        # Check which process is using port 22

5. Tracing paths
traceroute google.com    # Trace the hops packets take
mtr google.com           # (install) combines ping + traceroute

6. DNS queries
nslookup google.com
dig google.com
dig google.com +short

7. Download & HTTP requests
curl http://example.com
wget http://example.com

8. Check firewall rules
sudo ufw status        # On Ubuntu/Debian
sudo iptables -L       # On systems with iptables
