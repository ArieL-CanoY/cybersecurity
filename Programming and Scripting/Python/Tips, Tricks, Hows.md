```python
# set end of line of print() to empty and not newline
	print('hello', end =' ')
	print('world')	# output hello world

# swapping 2 variables' values
	x = 12
	y = 10
	x, y = y, x

# printing strings
	# instead of this
	name = 'clem'
	age = 14
	print('Your name is ' + name + ', your age is ' + str(age))

	# do this
	name = 'clem'
	age = 14
	print(f'Your name is {name}, your age is {age}')

# generate random strings or numbers
	# strings
		rand_letters = ''  
		rand_letters =  rand_letters.join(rand.choice(string.ascii_letters) for i in range(20))
		# output is 20 characters long with lower and upper case letter

	# numbers
		rand_num = ''  
		rand_num =  rand_num.join(rand.choice(string.) for i in range(20))
		# output is 20 characters between 0-9 number

# if-else ternary one liner
	isValid = True if age >= 18 else False


# you can type the value of number like this: 1_8345_985 for readability
	num = 923_734_834






```



# f-string
```python
# print the number with separator by hundreds
	num = 1753
	print(format(num, ','))  # output is 1,753


# align text with column with space
	print(f'{"Name":<15}{"Age":<15}')
	print(f'{"Mark":<15}{18:<15}')


# print date like 03-14-2025
	import datetime
	now = datetime.datetime.now()
	print(f'{now:%d-%m-%y}')

# print the name of variable along with its value


```









# Functions
```python
# if you don't want to forget the function, use raise NotImplementedError
def printSomething():
    raise NotImplementedError('no function provided')
printSomething()


# specify the return type for readability and strict return type
def printSomething() -> str:
    return 'hello in the world'
word = printSomething()
print(word)

	# or you can specify the type of parametes
		def printSomething(num1: float, num2: float) -> float:
		    return num1 + num2
		result = printSomething(2, 5)
		print(f'{result = }')


# add documentation to the function when hovering the function call
def printSomething(num1: float, num2: float) -> float:
    '''
    :param num1: First number
    :param num2: Second number
    :return: float:  Sum of 1st and 2nd number
    '''

    return num1 + num2
result = printSomething(2, 5)
print(f'{result = }')


# assing value in the if condition
if num:= 13 >= 18:
	print('allowed')
else:
	print('not allowed')


# set a value to a single line and can be used later in the later line
# this is called walrus operator
print(word:= 'hello in the world', len(word) > 15)


# output specific error from the exception
num = 0
while True:
    try:
        userInput = input('Enter num: ')
        num += int(userInput)
        print(num)
    except Exception as e:
        print(repr(e))



# combined each iterable to be a tuple, useful when combining 2 iterables and converting it to a dictionary
numList = [1,2,3]
nameList = ['mark', 'vince', 'lumen']
result = zip(numList, nameList)
print(list(result))

	# output is [(1, 'mark'), (2, 'vince'), (3, 'lumen')]










```


















