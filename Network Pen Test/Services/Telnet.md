
Definition: [[Networking/Network Protocols/Telnet|Telnet]]


# Enumeration
```python
>> use nmap to scan ports


```


# Exploitation
```python
>> misconfigured telnet
	- sometimes telnet does not provide authentication mechanism and all you have to do is type this:
	telnet <target_ip> <port_it_listen_to(commonly 23)>
```



# Post-Exploitation
```python
>> .HELP <command>
	- get help for specific command

>> .RUN <command>
	- execute a command
	- you can create reverse shell using msfvenom
```

























