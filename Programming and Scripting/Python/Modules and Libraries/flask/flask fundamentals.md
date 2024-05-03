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

# Modules

### render_template
```python
# Note that this file is along with folder called html_files with 1 file called index.html

'''
here is the directory explanation:
> index.py
> html_files
  >> index.html
'''

from flask import Flask, render_template

app = Flask(__name__, template_folder="html_files")

@app.route("/")
def home():
    return render_template("index.html")

if __name__ == "__main__":
    app.run()

```


# File Upload
```python
from flask import Flask, render_template, request, redirect

app = Flask(__name__, template_folder="html_files")

@app.route("/")
def home():
    return render_template("index.html")

@app.route("/upload", methods=['POST'])
def upload():
    file = request.files['file']
    file.save(f'uploads/{file.filename}')
    return redirect("/")

if __name__ == "__main__":
    app.run()




```



# Secure File Upload 
```python
# import secure_filename from werkzeug.utils that remove any symbol before uploading it to the server

from flask import Flask, render_template, request, redirect
from werkzeug.utils import secure_filename

app = Flask(__name__, template_folder="html_files")

@app.route("/")
def home():
    return render_template("index.html")

@app.route("/upload", methods=['POST'])
def upload():
    file = request.files['file']
    file.save(f'uploads/{secure_filename(file.filename)}')
    return redirect("/")

if __name__ == "__main__":
    app.run()
```




























