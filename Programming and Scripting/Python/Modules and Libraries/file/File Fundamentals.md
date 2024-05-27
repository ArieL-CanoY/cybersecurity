# Notes
```python
if it returns an error of permission denied, check if the filepath is directory and not a file.
```


# Code
```python
# all the functions that call with read on it will return a string

# read the file and return it as a single string
with open(filePath, 'r') as file:
	contents = file.read()


# read the file and return single line, call the function again to return the next line
with open(filePath, 'r') as file:
	contents = file.readline()


# read the file every line as return every single line as a single element of a list
with open(filePath, 'r') as file:
	contents = file.readlines()


# truncate or change the file size of a file
with open(filePath, 'rb+') as file:
	file.truncate(123) # 123 value is for bytes


# write text on a file, if the filename does not exist, it will automatically created a new one
with open(filePath, 'w') as file:
	file.write('message')


# append or add text on a file
with open(filePath, 'a') as file:
	file.write('message')




```