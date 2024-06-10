
# Definition
```python
- stands for Hyper-Text Transfer Protocol
- use to transfer images, text, videos, sound from the web servers and present it to the client web browsers
- used TCP port 80 for unencrypted communication channel
- does not establish encrypted communications and all data sent across the internet or network is clear
- use for API request and response
- uses different methods to perform different request
- uses different status code for the status of response
```

to view more information, check [[HTTP (HyperText Transfer Protocol)]]




# Versions

### HTTP 0.9
```python

```


### HTTP 1.0
```python
- every resource that a client request to a server, it requires a new connection to be established which makes it resource intensive.
- request all files before it loads
```



### HTTP 1.1
```python
- introduce "Keep-Alive" connections, allowing clients to reused TCP connections without establishing another connections in each request
- only allow one (1) HTTP request and response at a time and not concurrent
```


### HTTP 2
```python
- uses one (1) TCP connection to request all resources in parallel (multiplexing)
- disadvantage is if a single file packet is loss, all other files are affected or will be loss also.
```


### HTTP 3
```python
- uses QUIC developed by Google and work at the transport layer using UDP
- quick streams are delivered independently and packet loss affecting one stream does not affect the others
- enhanced multiplexing and reduced latency
```





























