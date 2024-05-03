
# Mongo shell

# Notes
```python
- when calling a function, you should always put open and close parenthesis.
```

# Information
```python
>> show dbs
	- show all the databases


>> show collections
	- show all collections

>> typeof db.<collection_name>.findOne().<key>
	- this will return a value and evaluate to the typeof command which return specific data type.

>> db.<collection_name>.countDocuments({age: {$gte: 30}})
	- return the length of returned data





```

# Show Collection's data
```python

>> db.<collection_name>.find()
	- show all the data from specific collection

```
	
# Creation
- collection
```python
>> db.createCollection("<collection_name>)
	- create a collection

>> db.<collection_name>.insertOne({<key>:<value>})
	- when the collection is not created, it automatically created and insert the data.
	- the <key> can be specify without quotes and automatically remove it once the insertion returns true.





					   
```

# Insertion
```python

>> db.<collection_name>.insertOne({<key1>:<value1>, <key2>:<value2>})
	- insert multiple keys and values in one object

>> db.<collection_name>.insertMany([{<key>: <value>}, {<key>: <value>}])
	- insert many data from a single collection.

>> db.<collection_name>.insertMany([{<same key>: <value>}, {<same key>: <value>}], {<different key>:<value>})
	- insert many data or single data with another different key.

	

```


# Selection
```python
>> db.<collection_name>.find({})

>> db.<collection_name>.find_One({<key>:<value>})

>> db.<collection_name>.find().sort({<key_to_sort>: <option>})
	option:
		1 - ascending
		2 - descending

>> db.<collection_name>.find().skip(<n1>).limit(<n2>)
	n1 - number of returned data or rows to skip
	n2 - number of returned data or rows to get

>> db.<collection_name>.find({<key>: <value>}, {<key_to_get_its_value>: 1 <option>})
	option:
		, <another_key>: 1 - get another value based on their key
		- _id: 0 - do not return the id because it automatically return it when you do not specify.
		- if you want to return the value of that key, you can remove the value 1

>> db.<collection_name>.find({<key>: <value>}, {<get_all_key_other_than_this>: 0})
	- get all the value of every keys other than specified with value of 0.
```


# Selection with Condition
```python
>> db.<collection_name>.find(<key>: {$<option>: <value>})
	option:
		$eq - equal to 
		$ne - not equal to
		$gt - greater than
		$gte - greater than or equal to
		$lt - less than
		$lte - less than or equal to
		$in - if the value of key is in the list
			ex:
				db.users.find({username: {$in:["mark", "kyle", "crane"]}})
		$nin - if the value of key is not in the list then return all of it

>> db.<collection_name>.find({<key>: {$exists: true}})
	- return all of the data if the key exists from them
	- you can also change it to false
	- note that even the value is null, it will return the data


# AND query
>> db.<collection_name>.find({age: {$gte: 18, $lte: 30}})
>> db.<collection_name>.find($and: [{username: "mark"},{age: 28}])
	- find data in the collection where username is equal to "mark" and age is equal to 28

# OR query
>> db.<collection_name>.find($or: [{username: "mark"},{age: 28}])
	- find data in the collection where username is equal to "mark" or age is equal to 28

>> db.<collection_name>.find($expr: {$gt: ["$<key>","$<another_key>"]})
	- compare if the key is greater than another_key field




	
```


# Updating
```python

# normal update - update specific value from a field
>> db.<collection_name>.updateOne({<keyToFind>: <valueToFind>}, {$set: {<keyToFind>: <valueToReplace>}})
	ex:
		db.users.updateOne({age: 18},{$set: {age: 28}})
			- change the user with age 18 to be 28



# increment the value from the collection
>> db.<collection_name>.updateOne({<keyToFind>:<valueToFind>},{$inc: {<keyToFind>:<valueToIncrement/Add>}})
	ex:
		 db.users.updateOne({username:"mojang84_"},{$inc: {points:30}})
			- increase the points by 30 with the username "mojang84_"

# update the name of a column or field
>> db.<collection_name>.updateOne({<keyToFind>:<valueToFind>}, {$rename: {<keyToFind>:<valueToReplace>}})
	- update the name of a column or a field based on the first object argument.


# adding or appending new value to an array
>> db.<collection_name>.updateOne({username: "mojang84_"}, {$push:{<keyWithValueOfArray>:<valueToAdd>}})
	- find the username "mojang84_" then add new value to its keyWithValueOfArray key


# removing a value to an array
>> db.<collection_name>.updateOne({username: "mojang84_"}, {$pull:{<newKeyWithValueOfArray>:<newValueToAdd>}})
	- find the username "mojang84_" then remove a value to its keyWithValueOfArray key

	ex:
		from {'username': 'mark'}
		then running updateOne({'username': 'mark'}, {'$push': {'age': 28}})
		to   {'username': 'mark', 'age': 28}
		


# update many collections
>> db.<collection_name>.updateMany({username: {$exists: true}}, {$unset : {username: ""}})
	- update all the collections with field of username to remove its username field
```


# Deleting
```python
>> db.<collection_name>.deleteOne({username: "mojang84_"})
	- delete single data or document that the username is equal to "mojang84_"

>> db.<collection_name>.deleteMany({username: "mojang84_"})
	- delete multiple data or documents that the username is equal to "mojang84_"



```



# Dropping database
```python
>> db.dropDatabase()
	- drop the current use database 
```




















