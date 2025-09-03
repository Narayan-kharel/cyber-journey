1. Check your IP address
ip addr


Example output:

2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500
    inet 192.168.1.100/24 brd 192.168.1.255 scope global eth0


inet → IPv4 address (192.168.1.100).

lo → loopback (127.0.0.1).

👉 Old command: ifconfig (may need sudo apt install net-tools).

2. Test connectivity
ping -c 4 google.com


Example output:

PING google.com (142.250.70.14): 56 data bytes
64 bytes from 142.250.70.14: icmp_seq=1 ttl=118 time=12.3 ms


-c 4 → send only 4 packets.

Useful to check if network/DNS works.

3. DNS lookups
nslookup google.com


or

dig google.com


Example output:

Name:    google.com
Address: 142.250.70.14

4. Routing table
ip route


Example output:

default via 192.168.1.1 dev eth0
192.168.1.0/24 dev eth0 proto kernel scope link src 192.168.1.100


Shows your default gateway (router).

5. Open connections & listening ports
ss -tuln


Example output:

Netid State  Local Address:Port   Peer Address:Port
tcp   LISTEN 0.0.0.0:22            0.0.0.0:*
udp   LISTEN 127.0.0.1:123         0.0.0.0:*


t → TCP

u → UDP

l → listening

n → show numbers, not names

👉 Old command: netstat -tuln

6. Download from the internet
curl https://example.com
wget https://example.com/file.txt


curl → fetches webpage output in terminal.

wget → downloads file.