
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

>> db.<collection_name>.insertMany([{<key>: <value>}, {<key>: <value>}])
	- insert many data from a single collection.

>> db.<collection_name>.insertMany([{<same key>: <value>}, {<same key>: <value>}], {<different key>:<value>})
	- insert many data or single data with another different key.

>> d

```


# Selection
```python
>> db.<collection_name>.find({})


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

	
```


# Show Collection's data
```python

>> db.<collection_name>.find()
	- show all the data from specific collection

>> 












```


# Dropping database
```python
>> db.dropDatabase()
	- drop the current use database 



```




















