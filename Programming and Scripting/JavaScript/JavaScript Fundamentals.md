
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



# Operators
```javascript
let num = 4 + 2;  // num value is 6

let num = 4 - 2;  // num value is 2

let num = 4 * 2;  // num value is 8

let num = 4 / 2;  // num value is 2
```


# Increment and Decrement
```javascript
let x = 12;
x++;  // x value is 13

let x = 12;
x--;  // x value is 11

```



# Augmented Assignment Operator
```javascript
>> Addition
	let x = 12;
	x += 8;  // 20


>> Subtraction
	let x = 12;
	x -= 8;  // 4


>> Multiplication
	let x = 12;
	x *= 8;  // 96


>> Division
	let x = 12;
	x /= 8;  // 1.5


>> Modulus
	let x = 12;
	x %= 8;  // 4
```



# String Escape
```python
` backtick - use to escape both single and double qoutes

commonly use backward slash:
\"
\'
\\
\n
\r
\t
\b
\f


```



# Array
```javascript
- can store any data type
- mutable; its data can be change by accessing its value/element by index then change its value.


-------------- Normal Array --------------

let names = ['mark', 'vince', 'aiden', 'pearce'];
console.log(names[2]);  // aiden



-------------- Nested Array --------------
let groups = [['mark', 'aiden'], ['vince', 'pearce']];

// group 1
console.log(groups[0][0]);
console.log(groups[0][1]);

// group 2
console.log(groups[1][0]);
console.log(groups[1][1]);


/*
output is:
	mark
	aiden
	vince
	pearce
*/



-------------- Change Value --------------
let names = ['mark', 'vince', 'aiden', 'pearce'];
console.log(names[0]);  // mark
names[0] = 'josh'
console.log(names[0]);  // josh






```





# --------- Loops ---------
# For Loop
```javascript


```



# While Loop
```javascript

```



# ForEach
```javascript

```


# Function
```javascript
function passwordLengthValid(password)
{
	return String(password).length >= 8;
}

let password = 'password@123!';
let passwordValid = passwordLengthValid(password);
console.log(passwordValid);


```
















