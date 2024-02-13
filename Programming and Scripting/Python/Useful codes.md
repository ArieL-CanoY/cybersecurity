```python
# This is single comment

#Declaration and data type
	x = 4                                      #integer
	x = 1.23                                   #float
	x = true                                   #boolean
	x = 'hello'                                #string
	x = ["apple", "banana", "cherry"]          #list
	x = ("apple", "banana", "cherry")          #tuple
	x = {"apple", "banana", "cherry"}          #set
	x, y, z = 1, 'hello', True


#Conversion
	#float to int
		int_var = int(float_var)
	#int to float
		float_var = float(int_var)
	#int to string
		string_var = str(int_var)
	#string to int
		int_var = int(string_var)
	#string to bool
		bool_var = bool(string_var) # empty == False, non-empty == True
	
#printing
	print(x)

	#always convert other type when printing with string
	a = True
	b = 10.33
	c = 303
	print('a is : ' + str(a))
	print('b is : ' + str(b))
	print('c is : ' + str(c))


#functions
	str(var)                 #convert variable to string
	int(var)                 #convert to int
	bool(var)                #to bool
	float(var)               #to float
	len(var)                 #size of character - useful for string
	type(var)                #identify the data type


#string
	x = 'hello world'

	#print or get specific character on string 
	print(x[1])        #output is e, start from 0

	#looping the character 
	for y in x:
		print(y)       #output is print hello world including space vertically

	#print or get character length
	print(len(x))

	#check if string contains a specific string or character - return as bool type
	x = 'hello world'
	isContains = 'world' in x
	print(isContains)     #return true

	#if not contains
	x = 'hello world'
	isContains = 'world' not in x
	print(isContains)     #return false

	#slice
	x = 'hello world'  
	print(x[0:5])         #output is hello, start from 0 end in 4
	
	print(x[:5])          #shortcut, it means from the start, vice versa

	#upper and lower
	print(x.upper())
	print(x.lower())

	#split - convert each word to elements of list
	x = 'hello world'
	x_split = x.split()

	print(x_split[0])       #output is hello
	print(x_split[1])       # output is world

	
	#replace, remove whitespace
	x = 'hello world'
	print(x.replace('h','b'))         #output is bello world

	print(x.replace(' ', ''))         #remove space, output is helloworld


	#formatting
	quantity = 3  
	itemno = 567  
	price = 49.95  
	myorder = "I want to pay {2} dollars for {0} pieces of item {1}."  
	print(myorder.format(quantity, itemno, price))


	#escape string
	print('\'hello\'')        #output is 'hello'
	print('\\hello\\')        #output is \hello\
	print('hello\nworld')     #output is hello(newline)world   
	print('hello\tworld')     #output is hello    world - add tab space  
	print('hello\b world')     #output is hell world   

	
	#string functions:
```
![[Pasted image 20221217092142.png]]
![[Pasted image 20221217092158.png]]
![[Pasted image 20221217092217.png]]

```python
#Booleans
	print(10 > 5)             #output is True
	print(10 > 20)            #output is False
	print(10)                 #0 and 0.000... is False, else True
	print('de')               #' ' or empty is False, else True
	print('aa' == 'aa')       #output is True

#Operators
	#Arithmetic
		print(1 + 4)            #output is 5
		print(5 - 1)            #output is 4
		print(5 * 1)            #output is 5
		print(11 / 2)           #output is 5 - int
		print(5 % 2)            #output is 1, means remainder
		print(2 ** 2)           #exponent 2^2 == 4
		print(12 // 2)          #output is 6 - float


	#Assignment
		x = 2
		y = 4
		z = x          #z is x value
		z += x         #z = z + x
		z = z + x      #same as the above
		y += x         #y = y + x
		y -= x         #y = y - x
		y *= x         #y = y * x
		y /= x         #y = y / x
		y **= x        #y = y ** x

	#Comparison
		==             #equal to
		!=             #not equal
		>              #greater than
		<              #less than
		>=             #greater than or equal
		<=             #less than or equal


	#Logical 
		and            #all value should be true to be true
			print(7 > 3 and 1 == 1)   #True
		or             #one must be true to be true
			print(8 == 10 or 1 == 2 or ((3-1) == 2))   #True
		not            #reverse the result
			print(not False)   #True
			print(not 1==1)    #False


	#Identity
		is                 # same as ==
		is not             # same as  !=


	#Membership
		in                 #use in string if it contains
			x = 'hello world'
			print('world' in x)   #True
		not in                 #use in string if it contains
			x = 'hello world'
			print('world' not in x)   #False
		

#List
	#assigning
	mylist = ["apple", "banana", "cherry"]  
	print(mylist)         #output all elements

	app, bana, cher = mylist     #assign 3 variable 

	#access individual
		print(mylist[1])  #banana

	#size or length or list
		print(len(mylist))
		
	#contain different data type
		mylist = ['yes', 12, 19.22, True, (23==23)]

	#contain
		if 'apple' in mylist:            #Yes
			print('True')

	#change value
		mylist[0] = 'ball'
		mylist[:2] = ['black', 'ball', 'pen']

	#insert
		mylist = [1,2,3,4,5]
		mylist.insert(2:, 93)
		print(mylist)             #1,2,93,3,4,5

	#add items
		mylist = [1,2,3]
		mylist.append(4)
		print(mylist)             #1,2,3,4

	#extend or join or merge 
		list1 = [1,2]
		list2 = [3,4]
		list3 = list1.extend(list2)
		print(list3)            #1,2,3,4

	#remove items 
		list1 = [1, 2, 3]
		list1.remove(2)            #specific items
		list1.pop(1)               #by index
		del list1[1]               #same as above
		del list1                  #delete the list

		list1.clear()              #clear all items
		
	#loop
		list1 = [1, 2, 3]
		for x in list1:
			print(x)                   #1 2 3 each with newline


	#sort
		list1 = [3,7,4,1,9]
		list1.sort()                   #1,3,4,7,9
	
			#case-sensitive
				list1 = ['banana', 'Apple']        
				list1.sort()         #banana, Apple
	
			#case-insensitive
				list1.sort(key = str.lower)   # Apple, banana

	#reverse order
	list1 = [1,2,3,4,5]
	list1.reverse()                #5,4,3,2,1


	#copy
		list1 = [1,2,3]
		list2 = list1.copy()
		#or 
		llist2 = list(list1)


	#index of
	list1 = [1,2,3,4]
	list1Index = list1.index(3)         #return 2




	



```