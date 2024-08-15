
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



















