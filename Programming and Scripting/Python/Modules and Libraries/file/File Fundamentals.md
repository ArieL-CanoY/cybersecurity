# Notes
```python
if it returns an error of permission denied, check if the filepath is directory and not a file.
```


# Code
```python
# reading file every line
with open(filePath, 'r') as file:
	file.readlines()


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