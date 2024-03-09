```python
# import the library of sqlite
import sqlite3

# make a connection to the database
# this will open or create the database if not exists
dbConnection = sqlite3.connect('<filepath of connection or to be created>')

# create a cursor for executing queries
cursor = dbConnection.cursor()

# create table query
cursor.execute('CREATE TABLE IF NOT EXISTS account (username text, password text)')

# insert query
cursor.execute(f"insert into account values ('{username}', '{password}')")
# or
cursor.executemany('insert into account values (?, ?)', listOfData)

# select query
datas = cursor.execute(f"select username from account where username = '{username}'")
# or
datas = cursor.execute('select username from account where username={?}', username)

# after selecting, iterate the values
# the return type of cursor.execute() is tuple, so you can access multiple column using index - data[indexNum]
for data in datas:
	print(data)


# after query, you should close the cursor
cursor.close()


# close the database connection once the query is executed
dbConnection.close()

```
































