
# Definition
```python
- Hydra is a powerful, fast, and flexible password cracking tool included in Kali Linux, a popular penetration testing distribution. It is used for brute-force attacks on various network protocols to find valid login credentials. Hydra supports numerous protocols, including but not limited to HTTP, HTTPS, FTP, SMTP, SMB, and MySQL.
```


# Usage
```python
>> hydra [options]


options:
	-l LOGIN or -L FILE  login with LOGIN name, or load several logins from FILE
	-p PASS  or -P FILE  try password PASS, or load several passwords from FILE
	-C FILE   colon separated "login:pass" format, instead of -L/-P options
	-M FILE   list of servers to attack, one entry per line, ':' to specify port
	-t TASKS  run TASKS number of connects in parallel per target (default: 16)
	-U        service module usage details
	-h        more command line options (COMPLETE HELP)



>> hydra -t 4 -l dale -P /usr/share/wordlists/rockyou.txt -vV 10.10.10.6 ftp
	- 


```




























