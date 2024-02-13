- stands for Network Address Translation
- used to translate Private IP address into Public IP address
- because of the growing number of devices connecting to the network, people see that the IPv4 address can no longer sustain in the future so they make classification of IP address which are the Public and the Private addresses
- the idea is the devices on the LAN will only use 1 Public IP address and track using the NAT table 
- Private Addresses are:
	- Class A - 10.0.0.0 - 10.255.255.255
	- Class B - 172.16.0.0 - 172.31.255.255
	- Class C - 192.168.0.0 - 192.168.255.255
-  These Private Addresses can only be use within internal network


Sending a data to the outside:
![[NAT sending data.png]]

When the data comes back:
![[NAT receiving data.png]]


#### Dynamic NAT
- instead of using 1 Public IP address, it will use a pool 


