
# User-defined Modules
note: both file are in the same directory


message.py - module to be used
```python
def welcome():
    print('Welcome to Python Messages')

def bye():
    print('Bye to Python Messages')

```


script.py - file to call the module
```python
import message

message.welcome() # Welcome to Python Messages
message.bye()  # Bye to Python Messages



```

or 

script.py - file to call the module
```python
from message import welcome, bye # import method so that it will not call the class everytime we use it


welcome() # Welcome to Python Messages
.bye()  # Bye to Python Messages


```















# 



















