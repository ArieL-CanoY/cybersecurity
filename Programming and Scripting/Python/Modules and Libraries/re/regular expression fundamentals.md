
# patterns
```python

---------- Metacharacters ----------
\w - alphanumeric character - abcABC123_
\W - non alphanumeric character - *&^%$ including space and new line
\d - digit - 01374
\D - non digit - abcABC_*&^$
\s - space and new line
\S - all characters excluding space and new line



---------- Quantifiers ----------
+ - one or more
* - 0 or more 
{11} - 11 times
{8,} - 8 or more
{,3} - 0 min 3 max
{6,9} - min 6 max 9



---------- Wildcards ----------
. - any characters
? - optional, ex: words? - matches word or words - s is optional



---------- Start and End ----------
^The - a line that starts with 'The'
s\.$ - a line that ends with '.'
^None$ - a line that start and end with 'None'



---------- Escaping ----------
\<regex pattern> - treat it as normal string or character and not regex pattern
	ex:
		\^ - match a character ^ and not treat it as pattern 'start'
		\$ - same as above
		\[\] - same as above



---------- Group ----------
(\w)
[a-z0-9] - lowercase letter and number from 0-9
(pattern1|pattern2) - matches either pattern
	ex:
		(hello|hi) - matches 'hello' or 'hi'

```

# referring
```python
\<n> - refer to the matched string in a group
	ex:
		(\w+\d)\s\1
			should matched 'word23 word23', 'kig3 kig3' and should select the unique value 

$<

```

# important note
```python
\b\w{4}\b
	match exactly four words

anything that is between square brackets [] will treat as literal like [-.$\d]

[^abc] - match all other than a or b or c
	caret (^) in square brackets should be match

[a-b0-9] - matches a range of alphabets and digits

.* - greedy matches
.*? - not greedy matches



```

# Summary of look
```python
> positive lookbehind
	(?<=patternHere)

> negative lookbehind
	(?<!patternHere)

> positive lookahead
	(?=patternHere)

> negative lookahead
	(?!patternHere)
```


# positive lookbehind
- matches only characters with the behind pattern
```python
(?<=pattern_to_look_but_not_get)pattern_to_get



------------- example python code -------------
import re
textToSearch = '''This shows that occurrences of words like "quick" in the original text have been replaced with "nimble cat" according to the specified pattern.'''

pattern = r'(?<=").*?"\s(\w+)'
matched = re.findall(pattern, textToSearch)
print(matched)

# output: ['in', 'according']
```


# negative lookbehind
```python
(?<!pattern_to_look_but_not_get)pattern_to_get

import re
inputs = 'hello in the 999 world of programming'
pattern = r'(?<!the)\s(\w+)'
replace = 'yes'
result = re.findall(pattern, inputs)
print(result)


# output: ['in', 'the', 'world', 'of', 'programming']
```

# positive look ahead
- matches only characters with the ahead pattern
```python
pattern_to_get(?=pattern_to_look_but_not_get)


------------- example python code -------------
import re
textToSearch = '''This shows that occurrences of words like "quick" in the original text have been replaced with "nimble cat" according to the specified pattern.'''
pattern = r'\w+(?=\s".*")'
matched = re.findall(pattern, textToSearch)
[]()print(matched)

# output: ['like', 'with']
```

# negative lookahead
```python
pattern_to_get(?!pattern_not_to_look_and_not_get)


import re
inputs = 'hello in the 999 world of programming'
pattern = r'(\w+)\s(?!\d+)'
result = re.findall(pattern, inputs)
print(result)

# output: ['hello', 'in', '999', 'world', 'of']

```

# ----------------- Actual/Syntax ----------------****-
# search
- search a single string to be matched by the pattern specified.
- result.group() returns a single match - return string
- result.groups() returns the entire match - return tuple(string)
- result.start() returns the starting position of the match - return int
- result.end() returns the ending position of the match - return int

```python
import re
inputs = 'hello in the world123 hello888'
pattern = r'\w+\d+'
result = re.search(pattern, inputs)
print(result.group())

# output will be world123
```

- note that you can specify the group number index when your pattern has a group indicator "()" - group(0 or 1, etc.)

```python
import re
pattern = r'(\d{3}).*(\d{2}).*(\d{4})'
string = 'My number is 123-45-6789.'
match = re.search(pattern, string)
if match:
    print("Match found:", match.group())
    print("Area code:", match.group(1))
    print("Prefix:", match.group(2))
    print("Line number:", match.group(3))
else:
    print("No match found")

# output is:

# Match found: 123-45-6789
# Area code: 123
# Prefix: 45
# Line number: 6789
```


# findall
- find all the matched and return it as a list.
```python
import re
textToSearch = '''Hello in the-world *(&$% 8762368 _\n\n'''
pattern = r'\S+'
matched = re.findall(pattern, textToSearch)
print(matched)

# output
# ['Hello', 'in', 'the-world', '*(&$%', '8762368', '_']

```


# split
- result.split() returns just like .split() built-in method in python
```python
import re
inputs = 'hello in the world'
pattern = r'\s'
result = re.split(pattern, inputs)
print(result)

# output is ['hello', 'in', 'the', 'world']
```


# sub
- used to replace the matched string.
- note that it will replace all the string it matches
```python

import re
textToSearch = '''username@tryhackme.com'''
pattern = r'\.\w+'
sub = '.net'
matched = re.sub(pattern, sub, textToSearch)
print(matched)

# output: username@tryhackme.net


```

























