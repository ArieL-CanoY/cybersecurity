

# Definition
```python
- stands for Same-Origin Policy
- restricts how documents or scripts loaded from one origin can interact with resources from another origin.
- restricts a script from one origin to access properties and methods of a document from another origin.
- only the same origin can access their resource.
- origin defines this rules:
	- scheme or protocol: http, https
	- host: www.google.com
	- port: 443
	- if a request target server is not the same as the source, it automatically block by the web browser because of SOP.



```

# Example
```python
- if a script from "https://example.com" tries to access a resource from "https://another.com", the browser will block this action due to SOP.
```


# Header format
```python
todo
```


# Exceptions
```python
- Cross-Origin Resource Sharing (CORS)
	- Mechanism to relax SOP restrictions under specific conditions.

- Document.domain
	- Can be set to allow limited interaction between pages on subdomains.
```
























