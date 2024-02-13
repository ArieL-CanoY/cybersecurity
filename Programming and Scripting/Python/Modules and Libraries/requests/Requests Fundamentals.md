- a popular HTTP library for making HTTP request or to communicate with the web server using HTTP. 

installation
```python
note: type this on command line or shell:
	pip install requests
```


# Examples

#### Get requests
```python
url = 'https://www.google.com'
requests.get(url)

# for faster changing its url, set it to variable

# for faster calling its method, set it to variable
response = requests.get('https://www.google.com')
```

#### Print response body
```python
url = 'https://www.google.com'
requests.get(url)

# for shortcut, set it to variable then call the method .text, ex:
url = 'https://www.google.com'
requests.get(url)
print(response.text)
```

### Get Request and print response body
```python
import requests as req
url = 'https://www.google.com'
response = requests.get(url)
print(response.text)
```

#### Get status code
```python
url = 'https://www.google.com'
response = requests.get(url)

# for shortcut, set the requests.get(<url>) to a variable then call the variable for stauts code, ex:
response = requests.get('https://www.google.com')
print(response.status_code)
```


#### Post requests
```python
import requests as req

url = 'https://www.google.com'
requests.get(url)


```


# Allow and Disallow redirects
- if you want to know if the request is redirect, use this:
snippet:
```python
response = req.get(url, allow_redirects=False)
```

















