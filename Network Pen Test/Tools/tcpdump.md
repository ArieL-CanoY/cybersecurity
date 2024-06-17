
# Definition
```python
- a powerful command-line packet analyzer used for network traffic capture and analysis. It allows users to capture and display the packets being transmitted or received over a network to which the computer is attached.
```


# Usage
```python
>> tcpdump [options]

>> tcpdump host <local_ip_here>
	- capture packets from specific host

>> tcpdump port 80
	- captue packets on specific port of localhost

>> tcpdump 'tcp port 80 and host 192.168.1.1'
	- capture packets on specific host and specific port

options:
	-v                 - verbose; show more information. Use -vv to show more information
	port <port>        - capture packets from specific port
	tcp                - capture only TCP packets
	udp                - capture only UDP packets
	-i <interace>      - capture from specific interface. Ex: eth0
	-w capture.pcap    - write the captured packets information to a pcap file 
	
	



```





























