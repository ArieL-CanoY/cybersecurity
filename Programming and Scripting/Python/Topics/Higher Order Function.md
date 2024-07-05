
# Definition
```python
a higher-order function is a function that takes one or more functions as arguments or returns a function as a result.
```



# Example
### Function as an argument to execute
```python
def sayHi():
    print('Hi')

def sayHello():
    print('Hello')

def callFunction(function_name):
    function_name()

callFunction(sayHi)
callFunction(sayHello)
```



### Function as an argument with value to use
```python
def charLengthWithoutSpace(word: str) -> int:
    return len(''.join(word.split()))

def multiply(num1: int, num2: int) -> float:
    return num1 * num2

result1 = charLengthWithoutSpace("he lo")
result2 = charLengthWithoutSpace("the wo")
product = multiply(charLengthWithoutSpace("he lo"), charLengthWithoutSpace("the wo"))

print(product)
```



### Return the value of a function
```python
def outerFunction(value):
    def sayHi():
        print('Hi')

    def sayHello():
        print('Hello')

    if value == 'hi':
        return sayHi()
    elif value == 'hello':
        return sayHello()

outerFunction('hi')

```



### Return a function object
```python

def outerFunction(value):
    def sayHi():
        print('Hi')

    def sayHello():
        print('Hello')

    if value == 'hi':
        return sayHi
    elif value == 'hello':
        return sayHello

myfunc = outerFunction('hi')
myfunc()

```




















