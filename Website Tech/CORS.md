
# Definition
```python
- stands for Cross-Origin Resource Sharing
- security feature implemented by web browsers to control how web applications from different origin can interact with other.
- allows servers to specify which origins are permitted to access their resources, enabling secure cross-origin requests.
```


# Basics
```python
- An origin is defined by the combination of scheme (protocol), hostname, and port number
	- Example: https://www.google.com:443 and https://www.google.com:80 are considered as different origin.
```


# How it works
```python
- When a web application request to a different origin, the target server should configure what are origin are allowed to access their specific resource. This will include in the response header in the section "Access-Control-Allow-Origin".
- Preflight CORS is requesting the allowed methods to the server by using OPTION HTTP request method including the "Access-Control-Request-Method: POST_or_GET" that the server will respond all the allow methods using the header "Access-Control-Allow-Methods: method1, method2, etc." or can have a value of "*" which means all the methods which is risk because of "PUT" method
```



# Server's Response Headers
```python
>> Access-Control-Allow-Origin
	- in this header, it all includes all the origin that are permitted to request to the target web server specific resource. 
	- if the value is "*", then all other domain can access to any domain and subdomain of that target web server.
	- 
```
























