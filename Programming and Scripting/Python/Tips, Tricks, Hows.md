```python
#set end of line of print() to empty and not newline
	print('hello', end =' ')
	print('world')	#output hello world

#swapping 2 variables' values
	x = 12
	y = 10
	x, y = y, x

#printing strings
	#instead of this
	name = 'clem'
	age = 14
	print('Your name is ' + name + ', your age is ' + str(age))

	#do this
	name = 'clem'
	age = 14
	print(f'Your name is {name}, your age is {age}')

#generate random strings or numbers
	#strings
		rand_letters = ''  
		rand_letters =  rand_letters.join(rand.choice(string.ascii_letters) for i in range(20))
		#output is 20 characters long with lower and upper case letter

	#numbers
		rand_num = ''  
		rand_num =  rand_num.join(rand.choice(string.) for i in range(20))
		#output is 20 characters between 0-9 number

#if-else ternary one liner
	isValid = True if age >= 18 else False






```
































