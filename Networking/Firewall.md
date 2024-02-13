- can be either software or hardware
- designed to prevent unauthorized access from entering a private network
- blocks unwanted traffic and permits wanted traffic
- protect trusted network from untrusted network
- used to allow or block traffic depending the firewall rules or traffic rules
- firewall rules are like this and also known as ACL (Access Control List):
	 <html>
		 <body>
			 <table style="width: 100%; text-align: center;">
				 <tr>
					 <td style="border: 1px solid white;">Source</td>
					 <td style="border: 1px solid white;">Destination</td>
					 <td style="border: 1px solid white;">Port</td>
					 <td style="border: 1px solid white;">Action</td>
				 </tr>
				 <tr>
					 <td style="border: 1px solid white;">HOST A</td>
					 <td style="border: 1px solid white;">Any</td>
					 <td style="border: 1px solid white;">HTTP</td>
					 <td style="border: 1px solid white;">Allow</td>
				 </tr>
			 </table>
		 </body>
	 </html>

- Inbound traffic means the message coming from the outside the network, Outbound traffic means the message leaving from inside the network 
- most of the firewall are configured to block the incoming or inbound traffic. So what about the incoming traffic that are requested by devices inside the network? most firewall is stateful which means that it will allow the traffic to go inside the trusted network if that traffic is destined to the devices that requested a message before
- Next-Generation Firewalls (NGFWs) has additional security features like: 
	- Application Level Inspection where they can block risky application traffic
	- Intrusion Prevention System (IPS) that analyze the content traffic and look for patterns or signature like malicious or malware related traffic and it blocks it and anomalies or unusual traffic. 
	- Threat Intelligence where brand new malware identified can inform the firewall about this to be able to identify this new emerging threat 
- Firewall can also offer more features like URL filtering, email scanning, data loss prevention (DLP), etc. and firewall having these kinds of features can also called Unified Threat Management (UTM)

- Firewalls can be:
	- Software-based where the firewall is installed on the computer/device
	- Network-based where the firewall is installed on the network


2 types of inspection:
- Stateful
	- monitor all the connections and data streams that are passing through
	- keeps a record of previous data packets
	- does a thorough job of protecting a network dynamically

- Stateless 
	- does not do a thorough job
	- uses an ACL to allow or deny traffic
	- does not keep a record of previous data packets




- 




