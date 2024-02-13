
#### Definition:
- This module implements a common interface to many different secure hash and message digest algorithms. See more: https://docs.python.org/3/library/hashlib.html
- Secure hashes and message digests


# Note:
- Do not use SHA-1 and MD5 because it hashed collision.




# Examples:
```python
import hashlib 

msg = 'hello in the world'.encode('utf-8')  # declare a string and encode it in utf-8
hashed_object = hashlib.sha512(msg)
hashed_value = hashed_object.hexdigest()
print(hashed_value)





```

































































