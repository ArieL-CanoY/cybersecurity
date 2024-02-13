```python
# reading file
with open(fileAbsolutePath, 'r') as file:
	file.read()


# truncate or change the file size of a file
with open(fileAbsolutePath, 'rb+') as file:
	file.truncate(123) # 123 value is for bytes
```