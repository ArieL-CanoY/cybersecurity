```python
#slice
	x = 'hello world'
	print(x[:])  #hello world
	print(x[6:])  #world
	print(x[:5])  #hello

#strip - remove leading and trailing spaces
	x = '   hello world  '.strip()  #hello world
	
	x = '--hello-world--'.strip('-')  #hello-world

	#lstrip - leading
		x = '  hello world  '.lstrip()  #hello world
	
	#rstrip - trailing
		x = '  hello world  '.rstrip()  #  hello world

#removeprefix - remove the word from the start
	x = 'hello world'.removeprefix('hello')  # world

#removesuffix - remove the work from the end
	x = 'hello world'.removesuffix('world')  #hello 

#split
	x = 'hello world and yes'.split()  #['hello', 'hello', 'and', 'yes']

	x = 'hello and world and yes'.split(' and ')  #['hello', 'world', 'yes']

	#leading
	x = 'hello and world and yes'.split(' and ', maxsplit=1)  #['hello', 'world and yes']

	#trailing  
	x = 'hello and world and yes'.rsplit(' and ', maxsplit=1)  #['hello and world', 'yes']
#join
names = ['mm', 'mark', 'clem']  
combinedNames = '-'.join(names)  #mm-mark-clem

#uppercase, lowercase and capitalize
	#uppercase
	x = 'hello world'.upper()  #HELLO WORLD
	x.isupper()  #False
		
	#lowercase
	x = 'HELLO world'.lower()  #hello world
	x.islower()  #False

	#capitalize
	x = 'hello world'.capitalize()  #Hello world
	
#isalpha, isnumeric, isalnum
	x = 'python'
	print(x.isalpha(), x.isnumeric(), x.isalnum())  #True False True
	
	x = '101'
	print(x.isalpha(), x.isnumeric(), x.isalnum())  #False True True
	
	x = 'python101'
	print(x.isalpha(), x.isnumeric(), x.isalnum())  #False False True
	
	x = 'python_#101'
	print(x.isalpha(), x.isnumeric(), x.isalnum())  #False False False

#count
	x = 'hello world'.count('l')  #3
	
#find
	#start at the first index for finding
	x = 'hello world'.find('o')  #return 4 as index

	#specific index starting point of finding 
	x = 'hello world'.find('o', 5)  #return 7 as index

	#start at the last index for finding
	x = 'hello world'.rfind('o')  #return 7 as index

#starts and endswith
	x = 'hello world'
	x.startswith('he')  #True
	x.endswith('orl')  #False

#f-String
	name ='Clem'
	age = 19
	print(f'name is {Clem} and age is {age}')

#zfill
	x = '23'.zfill(4)  #0023

```