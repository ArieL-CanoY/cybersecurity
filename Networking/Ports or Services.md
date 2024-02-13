# Ports/Services
```bash
Telnet - Telecommunication Network
	- tcp 23
	- login to devices remotely
	- console access
	- in-the-clear communication means the message are sent in clear text
	- not the best choice for production systems



SSH - Secure Shell
	- tcp 22
	- encrypted communication
	- looks and acts like Telnet

  

DNS - Domain Name System
	- udp 53
	- converts name to ip addresses
	- www.google.com - 142.250.66.142
     

SMTP - Simple Mail Transfer Protocol
	- tcp 25
	- server to server email transfer
	- also used to send mail from device to mail server (configure in mobile devices and email clients)
     

IMAP4, POP3
	- clients receive email from email server
	- authenticate and transfer

  

POP3 - Post Office Protocol v3
	- tcp 110
	- basic mail transfer functionality

  

IMAP4 - Internet Message Access Protocol v4
	- includes management of email inbox from multiple clients

	  

SFTP - Secure File Transfer Protocol
	- tcp 22
	- use the same port as ssh
	- encrypted communication
	- uses GUI to transfer files

  

FTP - File Transfer Protocol
	- tcp 20 (active mode data)
	- tcp 21 (control)
	- transfer files between systems
	- authenticates with username and password
	- full-featured functionality (list, add, delete etc.)

  

TFTP - Trivia File Transfer Protocol
	- udp 69
	- very simple file transfer application
	- read and write files
	- no authentication
	- not used on production systems

  

DHCP - Dynamic Host Configuration Protocol
	- udp 67 (server)
	- udp 68 (client)
	- send information for ip configuration like ip address, subnet mask, default gateway, dns, etc.
	- Dynamic/Pooled of ip address that will to the client
	- set lease time for renewal of ip address
	- can reserve ip address based on the mac address of the client who wants ip address
	- automatically assign ip address on a network

  

HTTP - Hyper Text Transfer Protocol
	- tcp 80
	- communication in the browser
	- message sent in clear text
	- used by other application even not in browser

  

HTTPS - Hyper Text Transfer Protocol Secure

	- tcp 443
	
	- communication in the browser
	
	- message sent in encrypted
	
	- used by other application even not in browser

  

SNMP - Simple Network Management Protocol

	- udp 161 
	
	- gather statistics from network devices
	
	- v1
	
	  - the original
	
	  - in-the-clear
	
	- v2
	
	  - a good step ahead
	
	  - both transfer of data
	
	  - still in-the-clear
	
	- v3
	
	  - a secure standard
	
	  - message integrity
	
	  - authentication
	
	  - encryption
	


RDP - Remote Desktop Protocol

	- tcp 3389
	
	- remote desktop services on many windows application 
	
	- can connect entire desktop or just an application
	
	- clients for windows, macos, linux, unix, iphone, etc.

  

NTP - Network Time Protocol

	- udp 123
	
	- every devices has its own clock
	
	- synchronize the clocks
	
	- automatic updates 
	
	- flexible - you can control how clocks are updated
	
	- very accurate - better than 1 millisecond on a local network

  

SIP - Session Initiation Protocol

	- VoIP - Voice over IP Signaling
	
	- tcp 5060
	
	- tcp 5061
	
	- setup and manage VoIP sessions
	
	  - call, ring, hang up
	
	- Extend voice communication 
	
	   - video interferencing
	
	   - instant messaging
	
	   - file transfer
	
	   - etc.

  

SMB - Server Message Block 

	- Protocol used by microsoft windows
	
	- file sharing, printer sharing
	
	- also called CIFS (Common Internet File System)

NetBIOS - Network Basic Inpuut Output System

	- tcp 445 
	
	- direct SMB communication over tcp without NetBIOS transport

  

LDAP - Lightweight Directory Access Protocol

	- tcp 389
	
	- store and retrieve information in a network directory
	
  

LDAPS - Lightweight Directory Access Protocol Secure

	- tcp 636
	
	- a non-standard implementation of LDAP over SSL

  

H.323

	- tcp 1720
	
	- VoIP Signaling 
	
	- setup and manage VoIP sessions
	
	- one of the earliest VoIP standards
	
	- still in use today
	
  

DHCPv6 - Dynamic Host Configuration Protocol version 6

	- very similar process to DHCPv4 
	
	- udp 546 for client
	
	- udp 547 for server

	Process:
	
		DHCPv6 Solicit - client send multicast message to look for DCHP server on the network
		
		DHCPv6 Advertise - server send message to the client with associated IPv6 address
		
		DHCPv6 Request - client accept the advertise IPv6 message and send it back to the server
		
		DHCPv6 Reply - server gives the lease time and other IP configuration for IPv6 address










```


#### Other

```bash
UTM / All-in-one security appliance

		- Unified Threat Management (UTM) / Web security gateway
		
		- URL filter
		
		- Malware Inspection
		
		- Spam filter
		
		- CSU / DSU
		
		- Router, Switch
		
		- Firewall
		
		- IDS/IPS
		
		- Bandwidth shaper
		
		- VPN endpoint

  

Next-generation Firewalls (NGFW)

	-  can be called different names
	
	- stateful multilayer inspection
	
	- deep packet inspection
	
	- requires some advanced decodes
	
	- every packet must be analyzed, categorized, and a security determination






(Check evernote networking and networking 2 note for more information)
```