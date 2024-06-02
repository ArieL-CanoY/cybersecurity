
# Definition
```python
- stands for Cross-Origin Resource Sharing
- security feature implemented by web browsers to control how web applications from different origin can interact with other.
- 
```


# Basics
```python
- An origin is defined by the combination of scheme (protocol), hostname, and port number
	- Example: https://www.google.com:443 and https://www.google.com:80 are considered as different origin.
```


# How it works
```python
- When a web application request to a different origin, the target server should configure what are origin are allowed to access their specific resource. This will include in the response header in the section "Access-Control-Allow-Origin".
```



# Server's Response Headers
```python
>> Access-Control-Allow-Origin
	- in this header, it all includes all the origin that are permitted to request to the target web server specific resource. 
	- todo
```
























