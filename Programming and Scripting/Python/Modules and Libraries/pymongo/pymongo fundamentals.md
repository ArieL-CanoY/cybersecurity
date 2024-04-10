
# Note
- you can refer to MongoDb for query: [[MongoDB fundamentals]]

# Installation
```python
# windows
1. open cmd
2. type "pip install pymongo"
```

# Setup
```python
from pymongo import MongoClient

# connect to service
mongoClient = MongoClient('localhost', 27017)

# mongo db client database
db = mongoClient.get_database('mydatabase')
# or you can do this:
db = mongoClient['mydatabase']


# mongo db database's collection
collection = db.get_collection('mycollection')
# or you can do this:
collection = db['mycollection']


collection.insert_one({"username": "mark", "password": "password123"})

```


# Information
```python
documentLength = collection.count_documents({})
```


# Selection
```python
>> collection.find({'year': '2024'})
	- return all the objects that has a "year" key with a value of "2024"

>> collection.findOne({'year': '2024'})
	- return a single object that has a "year" key with a value of "2024"
	- suggested if only one data should be return




# iterate selection
datas = collection.find()
for data in datas:
	print(data) # object will print
	print(data.get('<key>')) # return all the data from specific key or field
	print(data['<key>']) # same as above



```

# Update
```python
filter = {'username': 'user1'}
update = {'$set': {'password': 'user1newpass'}}
status = collection.update_one({'username': 'user1'}, {'$set': {'password': 'user1newpass'}})

- update only the password of a username "user1"
- it will only update one data because of "update_one" function
- you can set another key with another value 





```

# Delete
```python
status = collection.delete_one({<key>:<value>})
print(status)
	- delete single data or a document


status = collection.delete_many({<key>:<value>})
print(status)
	- delete multiple data or documents


```

# Dropping database
```python
mongoClient.drop_database()

```





























