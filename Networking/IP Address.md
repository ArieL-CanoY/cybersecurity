- unique identifier assigned to each device connected to a computer network
- also called as logical address
- used to identify network and host on a network
- version 4 is common but gradually shift from version 6
- version 4 has a 32-bit separated by dot with 4 sections called octets: 192.168.123.45 - each octet or number can contain a number between 0-255 
- subnet mask is use by IPv4 address to identify network and host address on an IPv4 address
- there are different classes of IPv4 to make an address scalable and these are:
	- Class A - 1.0.0.0 - 126.255.255.255 with a subnet of 255.0.0.0
		- can have 16,777,214 hosts
	- Class B - 128.0.0.0 - 191.255.255.255 with a subnet of 255.255.0.0
		- can have 65534 hosts
	- Class C - 192.0.0.0 - 223.255.255.255 with a subnet of 255.255.255.0
		- can have 254 hosts

And that is Public IPv4 address. But because of the growing number of networks connecting to the internet, Private IPv4 address has been created:
	- Class A - 10.0.0.0 - 10.255.255.255 with subnet mask of 255.0.0.0
	- Class B - 172.16.0.0 - 172.31.255.255 with a subnet mask of 255.255.0.0
	- Class C - 192.168.0.0 - 192.168.255.255 with a subnet mask of 255.255.255.0

   Public IPv4 address range:
	   - 1.0.0.0 - 126.255.255.255 wi h subnet mask of 255.0.0.0
	   - 128.0.0.0 - 191.255.0.0 with subnet mask of 255.255.0.0
	   - 192.0.0.0 - 223.255.255.0 with subnet mask of 255.255.255.0
	   - 224.0.0.0 - 239.255.255.255
	   - 240.0.0.0 - 255.255.255.255

Private IPv4 address can use on different networks but Public IPv4 address should be unique, meaning a device can have:
136.235.23.65 Public IPv4 Address with a Private of 192.168.0.3
and other network which have Public IPv4 address of 184.123.45.51 with a Private IPv4 Address of 192.168.0.3

This will prolong the life of an IPv4 address because instead of using x number of x devices on our network, we can use 1 Public IPv4 Address on all devices on our network


169.254.0.1-169.254.255.254 - when a computer does not reach the DHCP, it automatically assign a private IP which is called protocol APIPA (Automatic Private Internet Protocol Addressing)