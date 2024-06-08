
```python
- A proxy is an intermediary server that separates end users from the websites they browse. Proxies provide varying levels of functionality, security, and privacy depending on your needs, company policies, or privacy concerns. They work by receiving requests from users, forwarding these requests to the relevant web servers, and then sending the retrieved data back to the users. This can help mask the user IP address, improve security, and manage network traffic.
```



# 2 types 

#### Forward Proxy
```python
- A forward proxy is positioned between a client and the internet. It receives requests from the client and forwards them to the appropriate web server. The responses from the web server are then sent back to the client through the proxy.
- Forward proxies are often used in corporate networks to manage employee internet usage, cache content to improve performance, and enhance security by blocking access to malicious sites.
- Requires a client to configure to forward its packet to the proxy.
- hierarchy:
	- client > forward proxy > internet > servers
```


#### Reverse Proxy
```python
- A reverse proxy is placed in front of web servers. It receives requests from clients on behalf of the web server and forwards these requests to the appropriate server. The responses from the server are then sent back to the clients through the proxy.
- Reverse proxies are used to load balance traffic across multiple servers, cache content to improve performance, handle SSL encryption, and protect web servers from direct exposure to the internet, enhancing security.
- hierarchy:
	- client > internet > reverse proxy > servers
```

























