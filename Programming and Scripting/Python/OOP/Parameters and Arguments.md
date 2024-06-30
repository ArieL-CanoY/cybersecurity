

# Basic 
```python
# no argument/s
def greet():
    print('Hello programmers')
greet()



# one (1) argument
def greet(name):
    print(f'Hello {name}')
greet('Vince')



# one (1) or more argument
def greet(name, age):
    print(f"Hello {name}, you are {age} years old.")
greet('Aiden', 28)



# arbitrary arguments or args
def greet(*names):
    for name in names:
        print(f'Hello {name}')

greet('mark', 'lumen', 'vince', 'pearce')



# keyword argument/s or kwargs
def greet(**user):
    for item, value in user.items():
        print(f'{item}: {value}')
    print(f'I am {user['name']} and I am {user['age']} years old.')

greet(name='Aiden Pearce', age=28)



# arbitrary and keyword arguments
# note that arbitrary arguments first before keyword because it will cause an error if not
def greet(*names, **user):
    for item, value in user.items():
        print(f'{item}: {value}')
    print(f'I am {user['name']} and I am {user['age']} years old.')
    for name in names:
        print(f'Hello {name}')

greet('mark', 'lumen', name='Aiden Pearce', age=28)



# passing a list values
def greet(names):
    for name in names:
        print(f'Hello {name}')

nameList = ['mark', 'vince', 'pearce', 'aiden']
greet(nameList)



# return keyword and statement 
def greet(name):
    return f'Hello {name}'

result = greet('Vince')
print(result)



# pass keyword
def greet():
    pass
greet()



# default value
def greet(name = 'vince'):
    print(f'Hello {name}')

greet()
greet('aiden')



# positional and keyword argument
def say(age):
    print(f'Age is {age}')
say(28)
say(age = 28)



# only positional argument and restrict keyword argument
def say(age, /):
    print(f'Age is {age}')
say(28)
say(age = 28)  # error



# only keyword argument and restrict positional argument
def say(*, age):
    print(f'Age is {age}')
say(28)  # error
say(age = 28)



# combine positional and keyword argument
def fillDetails(roomNumber, /, *, firstname, lastname):
    print(f'Room Number: {roomNumber}')
    print(f'First Name: {firstname}')
    print(f'Last Name: {lastname}')

fillDetails(115, firstname='Aiden', lastname='Pearce')






```






























