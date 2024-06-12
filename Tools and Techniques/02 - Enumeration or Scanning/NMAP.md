# NMAP - Network Mapper/Scanner

```python
Network Mapper - used for scanning network for open ports, vulnerabilities, information of a target machine and other protocols.


nmap [options] [options option value ] [host]

nmap [options] [host] [host] - scan multiple host 

nmap [host] [options]


-sP     - ICMP or Ping scan. Discover all host on a network (does not work if the target ICMP reply of host is off or blocked).

-sn     - ping scan. Does not work the a host is disable its ICMP reply or if it is blocked. Discover host on a network. Used ICMP protocol. Disable port scan after host discovery.

  

-Pn     - treat all host as online. Skip host discovery.

-sU     - UDP scan. Scan open UDP port of a target host.

-sT     - TCP connect scan. Used to scan host using 3 way handshake

-sS     - SYN stealth scan. Also called Half-Open scan. Does not complete 3 way handshake - 3rd step will reset the connection.

-sF      - Packet are sent in a Fin Flag (protocol for closing a port on a connection). Used to evade firewall.

-sV     - used to find out about specific service running on open port, it’s version and product Name. scan service/daemon versions

-sI      - use another host on a network to scan another host (do not know how to use right now)

-p [port/s (80,443, 1-65535)]      - scan specific port, can specific range of ports

-p-      - scan all ports

--top-ports [top number]      - scan the top or common ports protocols

-iL [text list of hosts]           - scan a list of hosts

-oN [filename of text want to save]               - save the output in a text file

-oG [filename of text want to save]               - save the output in a grepable way

-oX [filename of xml want to save]               - save the output in a xml file

-n       - disable reverse dns resolution for faster scanning. It works only within the network.

-A      - scan OS and service, version, script of a host

-T<0-5>      - the speed of scanning. The slower, the accurate.

--script [category]                 - scan using different category of scripts

--script=(script from nmap folder or http)          - scan using different scripts

-D RND:(number)      - generate random ip address as attacker

-D decoy1,decoy2...               - generate specific ip address as attacker

-sI [other ip from network] [target ip]          - use other ip from network as attacker

-F      - scan fewer ports than default scan ports. Scan top 100 ports

-sP -PA    - Ack Ping scan

-sP -PP     - TCP Ping scan

-sP -PS     - SYN Ping scan

--scanflags [Flags to be on like SYN,ACK]

--max-retries [number]          - number of retries when sending another ping probes when previous probe failed

--version-intensity [0-9]         - lower the slower

-O          - OS detection

-g/--source-port [port]          - change source port as an attacker to be act as legitimate traffic

-f           - turn the packet into smaller byte to evade firewalls

--mtu [packet value in byte]     - customize the size of packet that will transmit

--data-length [value]          -add data (by byte) to the probe or packet of scan to not determine that the packet is from nmap scan

--spoof-mac [0 is usually the value]     - generate random source mac address

--reason          - reason how the scan detect the port. ex. syn-ack

-r          - do not randomize port scan. Scan consecutively

-d/dd     - debugging mode (just like -v but more information)

  
```



#### NSE Scripts
```python
NSE (Nmap Scripting Engine) is a collection of scripts for advance scanning or use of nmap (like plugins in app or libraris in programming languages)


/usr/share/nmap/scripts/script.db - location to search for the collection of nse scripts

  

nmap --script [options] - use the scripts for the nmap

    (specific script from the nmap db) - use the specific scripts located on the database of the nmap directory

     Categories:

	     vuln - use the vulnerable scripts to find vulnerabilities on the network
	
	     safe - use for safe scanning of target machine
	
	     default - default category of a scripts


find more info about specific script:
	nmap --script-help <script_name>

	or cat specific script to see its description
	

  

  
```


# Installation of new script
```python
1. Download and output/put it to nmap scripts folder:
	sudo wget -O /usr/share/nmap/scripts/(script_name).nse https://svn.nmap.org/nmap/scripts/(script_name).nse

3. Update the NSE database(script.db) by typing the command:
	nmap --script-update 
```



#### List of good scripts 
```python
Scripts for vulnerabilities (download from github):

vulscan

vulners
```