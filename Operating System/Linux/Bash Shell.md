--- *bash shell* ---

To list all operators for comparison, type this:
```python
man test
```

Use 

Type of shell that can use to interact fully with the computer system 

```python
!/bin/bash 
	- always start of the bash file as the first code
```

# Quoting
#     Double Quote
```python
"" (Double quote) - The double quote ( "quote" ) protects everything enclosed between two double quote marks except $, \', \" and \. . Use the double quotes when you want only **variables and command substitution**.
- Characters like `$`, `\`, `"` and command substitution are still interpreted inside double quotes.

Working features:
Variable - Yes
Wildcards - No
Command substitution - Yes

Ex. 
The double quotes allowes to print the value of $SHELL variable, disables the meaning of [wildcards](https://bash.cyberciti.biz/guide/Wildcards "Wildcards"), and finally allows command substitution.

echo $SHELL - does print the value of $SHELL
echo "/etc/*.conf" - does not print all files in /etc with .conf
echo "Today is $(date)" - does print the output of date cmd

```


#     Single Quote
```python
'' (Single quote) - The single quote ( 'quote' ) protects everything enclosed between two single quote marks. It is used to **turn off the special meaning** of all characters.

Variable - No
Wildcards - No
Command substitution - No

Ex.
The single quotes prevents displaying variable $SHELL value, disabled the meaning of [wildcards](https://bash.cyberciti.biz/guide/Wildcards "Wildcards") /etc/*.conf, and finally command substitution ($date) itself.

# will treat all as strings inside the single quote
echo '$SHELL'  
echo '/etc/*.conf'  
echo 'Today is $(date)
```

#     Backslash
```python
\ (Backslash) - Use backslash to change the special meaning of the characters or to escape special characters within the text such as quotation marks.

Ex. 
You can use \ before dollar sign to tell the shell to have no special meaning. Disable the meaning of the next character in $PATH (i.e. do not display value of $PATH variable):  

echo "Path is \$PATH"   - escape the dollar
echo "Path is $PATH"    - treat as variable cause no escape


```

# Declaring variables
```python
name="Mark"

age=37

money=230934.2383

isTrue=false

# constant variable
readonly var=(value)

passwdFile="/etc/passwd"

```


# Printing variables
```python
name="mark"
age="19"
echo "Name is $mark and age is ${age}-year old"

# note
# use $var if printing it in a single word or only that value with space
# use ${var} if printing it with concatenation of other value without space

```


# Parameters
```python
ex. code - ./mybash.sh  arg1 arg2

   - get the first argument by $1 or the second by $2 ex. echo $2 will echo arg2 

ex. code - ./mybash.sh arg1 arg2 arg3 arg4  

   - get the number of arguments by $#
```



# Arrays
```python
names=('clem' 'mark')

access by ${name[@ for all/index number]}
	ex:
		${name[1]} - output mark



unset names[0]      - unset the name clem

names[0]='vince'     - set the first index to 'vince'




```



# Read input
```python

read -p "Enter your name: " name
echo "Your name is $name"  

options:
	-p [message] [var] - prompt message and input will store in variable

	-s                 - hide input, especially for passwrd
	-t [sec/s]         - cancel input if given time expire


```




# Operators Words

<html>
	<style>
		table{margin:100px;}
	</style>
	<body>
		<table style="border-spacing:10px; border: 1px black solid">
			<tr>
				<td style="border: 1px solid white">Operator</td>
				<td style="border: 1px solid white">Description</td>
			</tr>
			<tr>
				<td style="border: 1px solid white">-eq</td>
				<td style="border: 1px solid white" >checks if the value of the operands are equal or not; if yes then the condition becomes true.</td>
			</tr>
			<tr>
				<td style="border: 1px solid white">-ne</td>
				<td style="border: 1px solid white">checks if the value of two operands are equal or not; if values are not equal then the condition becomes true.</td>
			</tr>
			<tr>
				<td style="border: 1px solid white">-eq</td>
				<td style="border: 1px solid white">checks if the value of the left operand is greater than the value of right operand; if yes then the condition becomes true.</td>
			</tr>
			<tr>
				<td style="border: 1px solid white">-lt</td>
				<td style="border: 1px solid white">checks if the value of left operand is less than the value of right operand; if yes, then the condition becomes true.</td>
			</tr>
			<tr>
				<td style="border: 1px solid white">-ge</td>
				<td style="border: 1px solid white">checks if the value of left operand is greater than or equal to the value of the right operand; if yes, then the condition becomes true.</td>
			</tr>
		</table>
	</body>
</html>
---




# Operator Symbol
```python
>     - greater than
<     - less than
== or =   - equal to
>=    - greater than or equal to
<=    - less than or equal to
!=    - not equal to
```



# Arithmetic
```python
$((expression))
$((x + y))    - addition
$((x - y))    - subtration
$((x * y))    - multiplication
$((x / y))    - division
$((x % y))    - modulus
$((x++))      - post increment
$((x--))      - post decrement
$((x**y))     - exponential

search more

```


# Case switch

```python
case expression in
	pattern1)
		#code
		;;
	pattern2)
		#code
		;;
	*)
		#default value code
		;;
esac
```


# ---------- Conditionals ----------

#### ----- Arithmetic -----
```python
#!/bin/bash
echo '-----Comparing two numbers which is greater than-----'
echo 'Enter the first number:'
read firstNumber
echo 'Enter the second number:'
read secondNumber
if [ $firstNumber -gt $secondNumber ]; then 
			echo '$firstNumber is greater than $secondNumber'
elif [ $secondNumber -gt $firstNumber ]; then
	echo '$secondNumber is greater than $firstNumber'
else 
    echo '$secondNumber is equal to $firstNumber'
fi
```


#### ----- String -----
```python
read -p "Enter your input: " userInput

if [ $userInput = 'a' ]; then
        echo 'Yup, that is a'
else
        echo 'Nope, that is not a'
fi
```




# for loop
```python
valid:
	for var in $(command)
	for var in $var
	for var in  $((expression))

ex.
	for var in $var; do
		commands;
	done

	- loop a list of words
	for val in hello in the world; do
		echo $val;
	done


	- one line in terminal
	for val in hello in the world; do echo $val; done

	tips:
		- you can use the range shortcut to make multiple directories or files:
			touch file{1..10}


```


# Increment and Decrement
```python

((x++))
((y--))
```

# Function
```python


function_name()  # creation of function
{
	var  # variables
	command  # all commands
}

	function_name  # calling the fucntion



```
