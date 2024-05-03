
# Definition
```python
Definition source: python docs, chatgpt

The secrets module in Python is part of the Python Standard Library. It provides functions for generating secure random numbers suitable for managing data such as passwords, account authentication, and cryptographic keys. It is especially useful for generating cryptographically strong random numbers for sensitive operations.
```





# Random 32 characters 
```python
import secrets
import string

allCharacters = string.printable.strip()
print(allCharacters)

randomChoice = [secrets.choice(allCharacters) for num in range(32)]
print(''.join(randomChoice))
```

# All method

### Summary
```python
secrets.choice(stringOfCharacters)
secrets.randbelow(1000)  # 0-999
secrets.randbits(8)  # 0-255
secrets.token_hex(8)  # 8 bits of hex - c6b87079f395a298
secrets.token_bytes(8)  # b'\xa7\xde8\xc4\x02\x16\xe65'
secrets.token_urlsafe()  # ROjhdQVI2SoFS1jEARnZvPeHbQT7lVOo-cZA-im1ejY
```






# Random number below
```python
import secrets

randomBelow = secrets.randbelow(1000)
print(randomBelow)

# Output: 0-999
```


# Random bits  
```python
import secrets

randomData = secrets.randbits(8)
print(randomData)

```


# Random token hex
```python
import secrets

randomData = secrets.token_hex(32)
print(randomData)

```



# Random token bytes
```python
import secrets

randomData = secrets.token_bytes(32)
print(randomData)
```

# Random safe URL
```python
import secrets

randomData = secrets.token_urlsafe()
print(randomData)
```























