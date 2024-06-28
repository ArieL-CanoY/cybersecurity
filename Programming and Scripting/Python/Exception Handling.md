

# Summary
```python
todo

>> ValueError:
	- function receives an argument with inappropriate type

	age = int('aiden pearce')
	print(age)


>> ZeroDivisionError:
	- when second argument is 0 when performing divison or modulo

	result = 10 / 0  # or result = 10 % 0
	print(result)


>> IndexError:
	- access index that does not exist

	numbers = [1, 2]
	print(numbers[10])

>> TypeError
	- operation receives an argument with inappropriate type

	result = 'hello' + 12
	print(result)

>>  NameError
	- using a variable that is not defined

	firstName = 'Aiden'
	print(age)

>> KeyError
	- accessing a value from a key that does not exist

	user = { 'name': 'Aiden Pearce'}
	userName = user['username']

>> AttributeError
	- calling a method of a class that does not exist

	mySet = {1, 2, 3, 4, 5}
	mySet.add(23)





```



# Other
```python
>> else
	- execute when there is no exception

	Ex:
		try:
		    result = 10 / 2
		    print(result)
		except ZeroDivisionError:
		    print('Cannot divide by zero.')
		else:
		    print('There is no exception.')




```




















