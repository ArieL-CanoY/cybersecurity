
# Variable Declaration
```javascript

>> var <variable_name> 
	- the variable and its value can be reassign 
	ex.
		var name = "Mark"; // declaration
		name = "Francis"; // allowed
		var name = "Vince"; // allowed


>> let <variable_name>
	- the value can be reassign but you cannot declare again its variable name.
	ex.
		let name = "Mark"; // declaration
		name = "Francis"; // allowed
		let name = "Vince" // not allowed
	

>> const <variable_name>
	- the name of variable and its value cannot reassign, it is fixed once it is declared, it will throw an error if reassign.
	ex.
		const name = "Mark"; // declaration
		name = "Francis"; // not allowed
		const name = "Vince" // not allowed
```


# Printing
```javascript
>> console.log("hello world");
```


# Comments
```javascript
>> Inline comment: // this is inline comment

>> Multiline comment:
	/*
		this is 
		multiline

		comment
	*/
```


# Data types 
```javascript
>> undefined
	- a variable that has no set value
	ex: 
		var number;


>> null
	- a variable that is explicitly set to a "null" value
	ex: 
		var number = null;


>> boolean
	- a variable with true or false value.
	ex: 
		var isPasswordValid = false;


>> string
	- a variable with text inside quote 
	- can be single or double quote
	ex: 
		var username = 'myuser123';
		//or you can use:
		var username = "myuser123";
		
>> number
	- can be integer or float
	ex:
		var grade = 94;
		var grade = 98.23;


>> array
	- collection of different data types
	ex:
		var cp_brand = ['vivo', 'oppo', 'infinix', 'samsung'];
		console.log(cp_brand[0]) // vivo

>> object
	- store key-value pairs
	

```































