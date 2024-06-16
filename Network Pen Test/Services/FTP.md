Definition: [[Networking/Network Protocols/FTP|FTP]]



### /var/ftp
```python
- commonly default directory where FTP service is running
```


# Exploitation
### Anonymous username
```python
- when connecting to a machine like this: ftp (IP), when asking for username, provide "anonymous" to see if the configuration of the server allow this.
- "anonymous" username is a type of access permission that allow user to not enter username and password.
- "anonymous" can lead to misconfiguration if the FTP server has sensitive files on it.
```





























