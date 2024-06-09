
# Definition
```python

- stands for Dynamic Host Configuration Protocol
- assigns IP addresses to hosts
- comes as a client and a server
- used UDP port 67 for server and UDP port 68 for client
- this protocol is created to automatically assign IP address and other configuration when a device connect to a network because before, they manually setup which take time when hundreds or thousands of computers are connecting to the network
- there are 2 ways of assigning IP address on a computer which are Static and Dynamic IP 
	- Static IP is assigned manually by a person and never changed whenever a device connect or disconnect to a network
	- Dynamic IP is assigned by a DCHP server and can be changed depending on the available IP address on a network
- each computer runs DHCP client which can request DHCP message to the DHCP server
- DHCP servers can run on routers or servers
- home router has built-in DHCP service but in enterprise is handle on a server/computer
- DHCP server's message has a configuration of IP address, Subnet Mask, Default gateway, DNS server and least time
- it lessen the time to configure devices on a network especially IP address should be unique on a network
- the range of the IP address is configured on the router setting or in the default gateway which has a start and end IP address
- you can reserve an IP address specific to a device using their MAC address. Reservations are typically given to special devices or computers, such as network printers, servers, routers, etc. so that they only have 1 specific logical address that every device on the network can easily know
- Process:
	- Note that socket is combination of IP address and Port
	- DHCP Discover - the client will send a broadcast with socket of 0.0.0.0:68 to 255.255.255.255:67 to discover where is the server running a DCHP service
	- DHCP Offer - the server with DCHP service is listening and when it got the Discover message, it sends a broadcast with socket of its IP address like 192.168.0.1:67 to broadcast address of 255.255.255.255:68 to tell if it has a available address and sends an offer of specific IP address
	- DHCP Request - after the client received the Offer message, it will send that it will accept the offer from socket of 0.0.0.0:68 to broadcast 255.255.255.255:67 on a network
	- DHCP Acknowledge - after the server received the Request message, it will Acknowledge it by giving an IP address, Subnet mask, Default gateway, DNS and lease time
- the lease time will tell when the IP address given to the device will expire and the device that received the IP address should inform the DHCP server to renew its IP address. This is to make sure that the IP address given will be available for other devices to connect to a network if the device does not renew their devices in a given time meaning they are not connected to the network anymore.
- DHCP relay is a protocol used in router to make a DHCP client request outside their subnet. When a DHCP client and server are on different subnet, when the client broadcast a request, it cannot go outside its subnet, but when the router is configured to have DHCP relay, it can send it to all of the other subnet or where the DCHP server where from. Other term is IP Helper
```


