# Definition
```python
- stands for Domain Name System
- it maps/convert/translate domain names into IP address. When typing any website name, our computer does not know of where to find that address because it needs an IP address, the message then will go to DNS server to find the IP of that website name and our computer will request on that IP address 
- this is created because humans can easily understand
- if you type website name and enter, the browser and the computer will check if they have local cache of that website with IP address, if there's nothing, it will send a query to the DNS server
```

# Query Process
```python
- The computer will send a query to the DNS Recursive Resolver manage by IP to see if they have the IP address of that website 
- If the Resolver does not have it, it will send a query to the Root name server which refer request to the Top Level Domain (TLD) server that has collection of TLD such as .com, .net, .edu, .gov, etc.
- The Resolver will then query a message to the TLD server which contain addresses of TLD servers and the Authoritative name server which has a specific website name
-  The Resolver will then query a message to the Authoritative Name Server and it will return the IP address of specific website 
- The Resolver will return the IP address back to the computer who request the IP address of the website
- The IP address will save to the local cache and browser of the computer who request the IP, and cache of the DNS Resolver
```

# Types of DNS Record
```python
	A - IPv4 address
	AAAA - IPv6 address
	CName - canonical name 
	MX - Mail Exchange
	NS - name server (authoritative)
	PTR - pointer which reverse DNS lookup
	TXT - text
```

---
source: https://www.cloudflare.com/learning/dns/what-is-dns/

- The query that is send to DNS Recursive Resolver is DNS Recursive Query

- 3 types of DNS queries:
	1. Recursive Query - In a recursive query, a DNS client requires that a DNS server (typically a DNS recursive resolver) will respond to the client with either the requested resource record or an error message if the resolver can't find the record.
	
	2. Iterative Query - in this situation the DNS client will allow a DNS server to return the best answer it can. If the queried DNS server does not have a match for the query name, it will return a referral to a DNS server authoritative for a lower level of the domain namespace. The DNS client will then make a query to the referral address. This process continues with additional DNS servers down the query chain until either an error or timeout occurs.

	3. Non-Recursive Query -  typically this will occur when a DNS resolver client queries a DNS server for a record that it has access to either because it's authoritative for the record or the record exists inside of its cache. Typically, a DNS server will cache DNS records to prevent additional bandwidth consumption and load on upstream servers.

# DNS Cache
```python
The purpose of caching is to temporarily stored data in a location that results in improvements in performance and reliability for data requests. DNS caching involves storing data closer to the requesting client so that the DNS query can be resolved earlier and additional queries further down the DNS lookup chain can be avoided, thereby improving load times and reducing bandwidth/CPU consumption. DNS data can be cached in a variety of locations, each of which will store DNS records for a set amount of time determined by a [time-to-live (TTL)](https://www.cloudflare.com/learning/cdn/glossary/time-to-live-ttl/).
```

The recursive resolver also has additional functionality depending on the types of records it has in its cache:

```python
1. If the resolver does not have the [A records](https://www.cloudflare.com/learning/dns/dns-records/dns-a-record/), but does have the [NS records](https://www.cloudflare.com/learning/dns/dns-records/dns-ns-record/) for the authoritative nameservers, it will query those name servers directly, bypassing several steps in the DNS query. This shortcut prevents lookups from the root and .com nameservers (in our search for example.com) and helps the resolution of the DNS query occur more quickly.

2. If the resolver does not have the NS records, it will send a query to the TLD servers (.com in our case), skipping the root server.

3. In the unlikely event that the resolver does not have records pointing to the TLD servers, it will then query the root servers. This event typically occurs after a DNS cache has been purged.
```


---

