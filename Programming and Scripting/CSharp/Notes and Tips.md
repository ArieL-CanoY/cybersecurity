
### Number output divide by hundred
```csharp
- used to output numbers by hundreds for more readability.

int price = 1024;
Console.WriteLine(price.ToString("N0"));  // 1,024


// or you can use this but very long code
Console.WriteLine(string.Format("{0:N0}", price));
```



### String Interpolation ($"{}" or in python - f-string)
```csharp
- used to concatenate or print values in a more flexible manner. 

ushort age = 28;
Console.WriteLine($"My age is {age}");
```



### Null Conditional Operator
```csharp
- used on conditions where the variable or objects can be null so it can have default values, by only using short code.

Example 1:
	string userName = null;
	string newUsername = userName ?? "default username";  // if the variable usernName is not null, then set it to variable newUsername, else it will default the value as "default username"
	Console.WriteLine(newUsername);  // because the userName is null, it will set the default value to "default username"



```


# Removing an object
```csharp
- there is a right way of removing an object

wrong way:


for (int ctr = 0; ctr < users.Count(); ctr++)
{
	if (users[ctr].username == "mark vince")
	users.RemoveAt(ctr);
}



```


# Conversion of time based on their CultureInfo
```csharp
Convert.ToDateTime(stringdatehere, CultureInfo.InvariantCulture);
```


# DateTime error
```csharp
sometimes, the error is the date format of the machine or computer, try to change from the format "day/month/year" to "month/day/year".
```


# Time of date set to 12:00:00
```c#
using System; // import


DateTime now = DateTime.Now.Date;
```


# Output all elements in one print
```c#
string itemCode = "234/344/543/431/455";
string[] itemCodes = itemCode.Split('/');
Console.WriteLine(string.Join(", ", itemCodes));
// output is 234, 344, 543, 431, 455

```


# String Split
```c#
- string "Split" function takes a char and not string

string itemCodes = allCodes.Split('/');
```


# Return a unique values of list of string
```c#
using System.Linq;

Console.WriteLine(duplicateStrings.Distinct().ToList());
```









