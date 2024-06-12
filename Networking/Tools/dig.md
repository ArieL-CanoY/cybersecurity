
# Definition
```python
- stands for "Domain Information Groper"
- an network administration tool used for querying DNS (Domain Name System) server. 
- commonly used to troubleshoot DNS-related issues, verify DNS configuration, and gather information about domain names and their associated DNS records.
- used to retrieve DNS records such as:
	- A (IPv4)
	- AAAA (IPv6)
	- MX (Mail Exchange)
	- NS (Name Server)
	- More


```



# Usage
```python
In Linux:
	dig (domain) - A record
	dig (dns server) (domain) (record type [A, AAAA, MX, NS, TXT]) - specific lookup


options:
	-x        - search for domain instead of IP. Ex: dig -x
	+trace    - trace all the paths when querying DNS
				
```


# Explain
```python
in the ANSWER SECTION like this:
google.com         157     IN       A          74.125.193.101


> google.com - domain we want to know the IP address
> 157 - TTL (Time To Live) in seconds that will expires once it stored on our local cache
> IN - in what record
> A - type of record we try to resolve or find
> 74.125.193.101 - resolved address 

```
























