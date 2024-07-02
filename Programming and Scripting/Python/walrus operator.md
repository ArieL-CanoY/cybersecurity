


# Basic
```python
if (userPassword := input('Enter your password: ')) == 'admin':
    print('Welcome Admin')
    print(f'Your password is {userPassword}')




```







# More faster than traditional
- without walrus operator, it can take up to 2.4 seconds
- with walrus operator, it can take only up to 0.58 - 0.72 second
- it can speed up the program by 60-75%


```python
import time

startTime = time.perf_counter()


def moreString():
    return 'hello in the world' * 200_000_000


# without walrus operator, comment the code below if you want to run with walrus operator

if len(moreString()) > 1000:
    print(moreString()[:(moreString().index('world', 1))])


# with walrus operator, comment the code below if you want to run without walrus operator

if len((myString := moreString())) > 1_000:
    print(myString[:(myString.index('hello', 1))])
    
endTime = time.perf_counter()
print(f'Time taken: {endTime - startTime}')

```













