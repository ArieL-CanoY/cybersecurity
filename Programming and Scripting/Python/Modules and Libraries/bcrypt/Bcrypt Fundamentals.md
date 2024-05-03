
# Installation
```python
# Windows
type this in cmd:
	pip install bcrypt

after you installed it, you can import it to the python script
```


# Implementation

### Hashing
```python
import bcrypt

# convert the string to byte first
userPass = b'password123'
# or you can use the <string>.encode('utf-8')
userPass = 'password123'.encode('utf-8')

hashedPass = bcrypt.hashpw(userPass, bcrypt.gensalt())
print(hashedPass)
```


### Checking Hashed
```python
import bcrypt


# convert the string to byte first
userPass = b'password123'
# or you can use the <string>.encode('utf-8')
userPass = 'password123'.encode('utf-8')
# provide the bcrypt_hashed by getting it from the database 
isPasswordCorrect = bcrypt.checkpw(userPass, <bcrypt_hashed>)
print(isPasswordCorrect)

```


# bcrypt.gensalt()
```python
bcrypt.gensalt is refer to the iteration of hashing algorithm to make the hashed more stronger and take a lot of time to crack by an attacker.

default value is 12, it accept integer from 4-31
```





























