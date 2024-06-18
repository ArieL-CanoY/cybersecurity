
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



# Arithmetic Operators
```javascript
let num = 4 + 2;  // num value is 6

let num = 4 - 2;  // num value is 2

let num = 4 * 2;  // num value is 8

let num = 4 / 2;  // num value is 2

let num = 4 ** 2;  // num value is 16
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



# Comparison Operator
```javascript
== - normal typing
=== - strict typing
!= - normal typing
!== - strict typing
>
<
<=
>=

normal typing - only the value should be the same and not the data type 
strict typing - the value and data type should be equal


```




# Logical Operator
```javascript
&&
||
!
```


# Membership
```javascript
in

ex:
	let nums = [34, 654, 2, 23456, 137, 1373456, 34, 345]
	if (2 in nums)
	    console.log('num exist');
	else
	    console.log('num not exist');
	//output is: exist

```



# Increment and Decrement
```javascript
let x = 12;
x++;  // x value is 13

let x = 12;
x--;  // x value is 11

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



# Array Methods
```javascript
-------------- array.push() --------------
- add a new element/value after the last element/value of an array

Example:
	let names = ['mark', 'vince'];
	names.push('aiden');
	console.log(names);  // output is ['mark', 'vince', 'aiden']



-------------- array.pop() --------------
- remove the last element or value from an array

Example:
	let names = ['mark', 'vince', 'aiden', ['pearce', 'edison']];
	var lastValue = names.pop();
	console.log(lastValue);
	var lastValuelastValue = lastValue.pop();
	console.log(lastValuelastValue);
	/*
	output is:
		[ 'pearce', 'edison' ]
		edison	
	*/


-------------- array.shift() --------------
- remove the first element or value from an array

Example:
	let names = ['mark', 'vince', 'aiden', ['pearce', 'edison']];
	var firstValue = names.shift();
	console.log(firstValue);  // output is mark



-------------- array.unshift() --------------
let names = ['mark', 'vince'];
names.unshift('aiden');
console.log(names);  // output is ['aiden', 'mark', 'vince']










```





# --------- Loops ---------
# For Loop
```javascript
for (let count = 0; count < 3; count++)
{
    console.log(count);
}
/*
output is :
	0
	1
	2
*/

```



# While Loop
```javascript
count = 0;
while (count < 3)
{
    console.log(count);
    count++;
}
/*
output is:
	0
	1
	2
*/


```



# ForEach
```javascript
let numbers = [8, 3, 4]
for (let num of numbers)
{
    console.log(num);
}


/*
output is:
	8
	3
	4
*/
```


# Conditional Statements
```javascript
syntax:
	if (condition)
		statement
	else if (condition)
		statement
	else
		statement





let num = '1';
if (num == 1)
	console.log('equal');
else
	console.log('not equal');
// output is: equal



----------- Strict Equality -----------
let num = '1';
if (num == 1)
	console.log('equal');
else
	console.log('not equal');
// output is: not equal





```



# Switched statements
```python
note:
	- put break on every case so that it will end the statement once it is evaluated, else it will execute the statement below.
	- you can disregard or not put "break" statement on default



Example:

	var continueProgram = 'y';
	
	switch (continueProgram)
	{
	    case "y":
	        console.log('Continue the program.');
	        break;
	    case "n":
	        console.log('End the program.');
	        break;
	    default:
	        console.log('Please type the required input.')
	}
	


```



# Object
```javascript

-------- an object --------
var user = {
    username: 'Aiden Pearce',
    password: 'aidenpearcepassword@123',
    email: 'aidenpearce123@gmail.com'
}

---- access property ----

// can be accessed by both of these:
var value = user.username;
var value = user['username'];



---- modify property ----
user.username = 'Mark Vince';




---- add property ----
// can add property using both of these:
user.contact = '09849394888';
user['contact num'] = '09849394888';


---- add property ----
// can delete property using both of these:
delete user.contact
delete user['contact num'];

```


# Array of Objects
```javascript

var user = [
    {
        "username": "Mark Vince",
        "email": "markvince@gmail.com",
        "contact": "0985747564",
        "hobbies": ["video games", "basketball", "tennis"]
    },
    {
        "username": "Aiden Pearce",
        "email": "aidenpearce28@gmail.com",
        "contact": "09429280773",
        "hobbies": ["chess", "swimming", "video games"]
    }
];

console.log(user[0].hobbies[2]);  // tennis


```




# Function
```javascript
----------- function -----------
function greet()
{
    console.log('hello world');
}
gree();  // hello world



----------- function with parameter -----------
function greet(name)
{
    console.log('hello ' + name);
}

let user = 'sarah';
greet(user)  // hello sarah




----------- function with parameter and return statement -----------
function passwordLengthValid(password)
{
	return String(password).length >= 8;
}

let password = 'password@123!';
let passwordValid = passwordLengthValid(password);
console.log(passwordValid);







```
















