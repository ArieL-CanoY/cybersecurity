# Installation
```python
# this is in windows
pip install flask
```


# Basic setup
```python
from flask import Flask
app = Flask(__name__)

@app.route('/')
def home():
	return '<h1>hello world</h1> '


if __name__ == '__main__':
	app.run()

# run this and it will automatically run a service on port 5000





```


# Payload
```python
@app.route('/output=<name>')
def OutputName(name):
	return f'hello {name}'
```


# Redirect
```python
from flask import Flask, redirect, url_for

app = Flask(__name__)

isAdmin = False

@app.route('/')
def home():
	return "this is home page"

@app.route('/admin')
def admin():
	if isAdmin:
		return redirect(url_for('actualAdmin'))
	else:
		return redirect(url_for('home'))

@app.route('/admin_kjasjKJHjJH8976JKhjkl876')
def actualAdmin():
	return "this is actual admin site"


if __name__ == '__main__':
	app.run()



```





