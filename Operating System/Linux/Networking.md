Learn computer networking first before learning this command, or you will lost at this path, I warn you..........youuuuu.......
```bash

ifconfig/ip a - display ip address configuration of ethernet

ip n/arp -a - neighbor

ip route show or ip route- 

ip route add 192.168.0.0/24 via 192.168.0.1       - add ip route 

route - show / manipulate the IP routing table|

iptables - administration tool for IPv4/IPv6 packet filtering and NAT

iwconfig - ip address configuration of wireless ethernet

arp -a/ip n - show the arp table

route/ip r - show the routing of router

netstat - display the network status, network connections, routing tables, interface statistics

	- l        - listening ports
	- a        - all ports

ss    - another utility to investigate sockets

     --route, -r - display the routing table, same result when using route -e

     --numeric, -n - show numerical addresses instead of trying to determine symboic host, names, ports, ...

     --listening, -l - display listening ports

     --tcp, -t - display tcp connection connected to the system

  

ping [ipv4 address or domain name] - check if computer/machine is reachable.Some machine icmp are disabled so              even it is reachable, it can say that, that machine is unreachable.

  

traceroute [ipv4 address or domain name]

whois [ipv4 address or domain name]

dig [ipv4 address or domain name]
	- x       - ?

nslookup [ipv4 address or domain name]

netdiscover -i [interface] - discover other machine on specific network address range



```



# DNS (Domain Name System)
```bash

/etc/resolv.conf - file for local dns (needs sudo to be write)

systemd-resolve --status - 

journalctl -u systemd-resolved
```

# firewall
```bash
note: if error occured, update and upgrade the system or package of ufw


sudo ufw enable        - enable the firewall 
sudo ufw disable        - disable the firewall 
sudo ufw allow [port]  - allow a port 
sudo ufw deny [port]  - allow a port 
sudo ufw status       - check the status of allow or disallow ports

sudo ufw default [allow | deny] [incoming | outgoing] 

sudo ufw deny proto tcp from [(ip address) | any] to any port 80,443 

sudo ufw status numbered
	sudo ufw delete [number]

```
