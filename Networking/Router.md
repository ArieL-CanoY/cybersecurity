- used IP address to route packets between different network
- routes data from one network to another based on their IP address
- used to connect different network
- it is a default gateway
- (to search further) when the last router got the message, it has the destination MAC address of the server
- At each hop, the router will update the destination MAC address of the packet to the MAC address of the next hop router or the destination device on the local network, depending on the routing decision.
- forward packets not destined to themselves

#### Routing
- Routing Table has a map of all the networks that routers know about and maintain it
- Routing Table contains routes with method, network address and interface
- Routing Table can be populated via three methods:
	1. Directly Connected 
		- Routes for the Networks which are attached
		- 
	2. Static Routes
		- Routes manually provided by an Administrator
		- 
	3. Dynamic Routes
		- Routes learned automatically from other Routers
- When Routers receive packets with an unknown Destination IP, packet is dropped
- it should be populated before a packet transmitted

#### ARP Tables
- everything with an IP has an ARP Table
- it should populate when a it is only needed while a packet is being transmitted



![[Pasted image 20230714085327.png]]


- Routers typically connected in a hierarchy
	- easier to scale
	- more consistent connectivity

- Hierarchy allows for Routes Summarization
	- Reduce number of Routes in Routing Table
	- Default Route - ultimate route summary
		- 0.0.0.0/0 - every IPv4 address
		- "for everything else, go here"
- 









