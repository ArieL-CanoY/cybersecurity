# note that this result an error and will check if the current version changed it

example code
```python
import time, threading

def samplefunction():
	print('hello world')
	time.sleep(1)
	
i = 1
threads = []

for i in range(10):
	thread = threading.Thread(target=samplefunction)
	thread.start()
	threads.append(thread)

for thread in threads:
	thread.join()
```

#### if there is argument in the function
```python
def function(message):
	print(message)

for num in range(10):
	msg = 'yes'
	thread = threading.Thread(target=samplefunction, args=msg)
```

#### if there are multiple arguments in the function
```python
def function(message, message1):
	print(message)

for num in range(10):
	msg = 'yes'
	msg2 = 'yes'

	thread = threading.Thread(target=samplefunction, args=(msg, msg2))
```


#### POST requests 
```python
import requests as req
url = 'example.login.com'

login_creds = {
	'username':'user1',
	'password':'password123'
}

response = req.post(url, data=login_creds)

print(response.text)
```


