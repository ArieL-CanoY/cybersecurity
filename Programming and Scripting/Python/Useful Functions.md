

```python
>> sorted(iterable)
	- return an ascending sort of items in a list type
	Example:
		numbers = (3, 7, 1, 5, 4)
		sortedGrade = sorted(numbers)
		print(sortedGrade)
		# output is [1, 3, 4, 5, 7]

		# you can also reverse it 
		numbers = (3, 7, 1, 5, 4)
		sortedGrade = sorted(numbers, reverse=True)
		print(sortedGrade)
		# output is [7, 5, 4, 3, 1]


		# you can also sort using a key on a dictionary
		people = [
		    {'name': 'mark', 'age': 28},
		    {'name': 'vince', 'age': 30},
		    {'name': 'aiden', 'age': 35},
		    {'name': 'pearce', 'age': 32}
		]
		
		sortedAge = sorted(people, key=lambda person: person['age'])
		print(sortedAge)
		# output is [{'name': 'mark', 'age': 28}, {'name': 'vince', 'age': 30}, {'name': 'pearce', 'age': 32}, {'name': 'aiden', 'age': 35}]



>> enumerate(iterable)
	- iterate an array with its index
	Example:
		mylist = [23.4332, 43.9545, 66.8431, 86.5534]
		for index, value in enumerate(mylist):
		    print(f'{index} - {value}')

		# output is:
			# 0 - 23.4332
			# 1 - 43.9545
			# 2 - 66.8431
			# 3 - 86.5534
		


>> map(function, iterable)
	- apply a specific function to each item in the iterable and return a list of it
	- put it on a list() function to return the list of its output
	Example:
		mylist = [23.4332, 43.9545, 66.8431, 86.5534]
		allRound = list(map(round, mylist))
		print(allRound)
		# output is [23, 44, 67, 87]

		# you can also use lambda to make it more flexible and not limited to function especially you want put arguments to a function
		mylist = [23.4332, 43.9545, 66.8431, 86.5534]
		allRound = list(map(lambda x: round(x, 2) + 1, mylist))
		print(allRound)
		# output is [24.43, 44.95, 67.84, 87.55]


		# if you don't want to use lambda, you can create your own function
		def myfunction(element):
		    return round(element, 2) + 1
		
		mylist = [23.4332, 43.9545, 66.8431, 86.5534]
		allRound = list(map(myfunction, mylist))
		print(allRound)    



>> filter(function, iterable)
	- use to filter an iterable using a function with condition of True or False
	Example:
		passingGrade = 75
		gradeList = [88.65, 75.76, 74.85, 73.99, 80.43]
		
		gradePassed = filter(lambda grade: grade > 75.0, gradeList)
		print(list(gradePassed))
		
		
		



>> zip(iterable, iterable)
	- combine two(2) iterable into single iterable, the same element on index will put on a single set
	- use list to view the list of sets
	Example:
		text = ['a', 'b', 'c', 'd', 'e']
		numbers = [1, 2, 3, 4, 5]
		combine = zip(text, numbers)
		print(list(combine))
		# output is [('a', 1), ('b', 2), ('c', 3), ('d', 4), ('e', 5)]
		






























```































