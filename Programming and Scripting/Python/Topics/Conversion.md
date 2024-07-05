
```python




# convert string to byte
string = 'password'
print(string)
print(type(string))
string = string.encode('utf-8')
print(string)
print(type(string))


# convert byte to string
string = 'password'
print(string)
print(type(string))
string = string.encode('utf-8')
print(string)
print(type(string))



# convert byte to hex
byteToHex = byteData.hex()

# convert hex to byte
hexToByte = byteToHex.encode('utf-8')
# or 
hexToByte = bytes(byteToHex, 'utf-8')

```
































