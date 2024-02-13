#### TCP/IP - Transmission Control Protocol
- is a set of rules, standards or guidelines on how devices will communicate to the network
- meaning Transmission Control Protocol/Internet Protocol
- this protocol is what we used today

All these functions are divided by different layers which are:
	- Application
	- Transport
	- Network
	- Physical - sometimes it is divided by Data Link and Physical


#### OSI - Open System Interconnect
- another model that is reference to TCP/IP because it has the same protocol or layer but has additional layer which are:
	- Application - SMTP, HTTP, HTTPS, FTP, SSH, DNS, DHCP
	- Presentation - Data Format, Encryption
	- Session - L2TP, RTCP, H.245, SOCKS
	- Transport - TCP, UDP
	- Network - IP, ICMP
	- Data Link - MAC
	- Physical - Cable, Ethernet


#### TCP vs UDP

TCP is reliable but slow
UDP is not reliable but faster  

Encapsulation is the process of putting headers and sometimes trailers in every layer when a client or server will send a message from top to bottom of the layer
	Process:
		Application - Data
		Transport - Data | L4 Header - TCP-segment/UDP-datagram
		Network - Data | L4 Header | L3 Header - packet
		Data Link - L2 Trailer | Data | L4 Header | L3 Header | L2 Trailer - frame
		Physical - the message above will travel to different networking devices using cables until the data gets to final destination

De-encapsulation is the process of opening the data in every layer when incoming message arrived from physical to application layer.
	Process:
		Physical - the message coming will travel to this layer like cable and continue to open just like the above until the specific data will be known
		Data Link - L2 Trailer | Data | L4 Header | L3 Header | L2 Trailer - frame
		Network - Data | L4 Header | L3 Header - packet
		Transport - Data | L4 Header - segment
		Application - Data

Encapsulation and De-encapsulation is done by all host on the network 



Using TCP, when the client request, the server respond and set bits of data to the client, example is it has to send an image, it will split it into 4 parts, and every part will split again into 4, first it will send the first part which has a 4 parts. If the client did not received the other part of that first part, it will send a message that it did not receive it which then the server will resubmit it. Then the second part will send and so on. The message or data that is sent is called segment

To establish a reliable connection, they must use 3-way handshake

1. Client will send SYN flag which means Synchronize to the Server
2. Server will send SYN ACK which means Synchronize Acknowledgement to the Client
3. Client will send Acknowledgement to the Server

TCP is typically use for web browsing, file transfer that needs reliable data transfer - connection-oriented
UDP is typically use for live and real time connection like video/voice call, gaming, etc.

TCP/IP original layers from top:
	1. Application
	2. Transport
	3. Internet
	4. Link

TCP/IP update layers from top:
	1. Application
	2. Transport
	3. Network
	4. Data Link
	5. Physical

## TCP Data Transfer
- when three-way TCP connection handshake is finished, when transferring data, it includes:
	- # Error-free data transfer
		- the sender calculate a packet/frame that will result as checksum to know at the end of the receiver what should data they would get, if the receiver, calculate the checksum of the data it got and does not match to the checksum on the data, it will ignore or discard it and no acknowledgement will sent to the sender. Because the sender does not received any acknowledgement at the given time, it will retransmit the data and receiver will calculate again the checksum
	- # Ordered-data transfer
		- TCP adds sequence of numbers in the TCP segments/Transport Layer that will used by the receiver to construct the actual form/sequence of packets in the correct order  
	- # Retransmission of lost data
		- every TCP segment that received, receiver will sent acknowledgement that it received the correct data from the sender, if no acknowledgement received by the sender with a give time, it will retransmit the TCP segment/data
	- # Discarding duplicate packets
		- the sender retransmit segment that it determines to be lost but is not, it can have duplicate segment sent, but the receiver can check the unique sequence number and it can determine if the current segment received is duplicate or not
	- # Congestion Throttling or Flow Control
		- when a significant number of packets have to be retransmitted or when the network is congested, it slows down the transmission of data to prevent packet loss and ensure that the network operates smoothly