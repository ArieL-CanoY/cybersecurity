

# Definition
```python
- in the context of web browsing, is a small piece of data sent from the web server to the client and stored for future used.
- cookies are used to manage session, meaning if you login to specific website, that website or server will give you session token inside the cookies so if you request a resource, the cookies with session token is your identity that you are permitted to access that specific resource.
- Other usage are the following:
	- personalization
	- tracking and analytics
	- advertising
```


# Notes
```python
- if a cookie is set with a domain attribute (e.g., "Domain=example.com"), it can be accessed by all subdomains of "example.com" (like "sub.example.com").
	- if the "Set-Cookie" header does not specify a "Domain" attribute, the cookies are available on the server that sets it but not on its subdomains

```


# Attributes
```python

>> Secure
	- a cookie with this attribute will only sent to the server with an encrypted request over the HTTPS protocol except on the localhost.


>> HttpOnly
	- this ensures that a JavaScript cannot modify a cookie such as using "Document.cookie", it can only modified when it reaches the server. 
	- also mitigate the session hijacking when the web server is vulnerable to Cross-Site Scripting (XSS) attacks.


```


























