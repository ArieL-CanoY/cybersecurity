Check out what is json: [[JSON]]



# Introduction
```python
- json is a built module on Python
- used to convert from json string to python dictionary or vice-versa
```

# Note
```python
convert it first to dictionary if you want to change its value then convert it back to json string.
```

# Json to Dictionary
```python
import json

jsonString = '''{"name": "mark", "age": 28}'''

jsonDict = json.loads(jsonString)
print(jsonDict)
print(type(jsonDict))

# output is:
	# {'name': 'mark', 'age': 28}
	# <class 'dict'>
```



# Dictionary to Json
```python
import json

jsonDict = {
    "name": "mark",
    "age": 28
}

jsonString = json.dumps(jsonDict)
print(jsonString)
print(type(jsonString))

# output is:
	# {"name": "mark", "age": 28}
	# <class 'str'>

```



# Load from a file
```python
import json

with open('data.json', 'r') as file:
    data = json.load(file)

print(data)
print(type(data))
```


# Write to a file
```python
import json

with open('data.json', 'r') as file:
    data = json.load(file)

# change something to that data
data['users'][0]['name'] = "NewName"

# write the data to a new filename
with open('data2.json', 'w') as file:
    json.dump(data, file)

```



# Adding indent to Json string
```python
import json

jsonDict = {
    "name": "mark",
    "age": 28,
    "isAdmin": False

}

jsonString = json.dumps(jsonDict, indent=4)
print(jsonString)

```


You can also sort its keys by putting "sort_keys=True"



















