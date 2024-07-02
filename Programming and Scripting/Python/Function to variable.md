- you can assign specific function to a variable, then calling that variable instead of the function
- it works like an alias


# Basic
```python
# assigning a user-defined function
def greet():
    print('Hello World!')

say = greet
greet()
say()



# assigning a built-in function
say = print
print('Hello Programmers')
say('Hello Programmers')


```
































