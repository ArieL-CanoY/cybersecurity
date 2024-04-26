- stands for regular expression

useful web: https://regexr.com/


# Summary
```python

	.              - any single character 
		ex. r.t    - look for r(any char)t - rotten, ratan 

	[pattern]      - specific pattern with or
		ex. b[ao]t - look for batallion or bottom
		 
	^pattern       - match that starts with
		ex. ^ca    - look for cat, canned carrier
			
	pattern$       - match that ends with
		ex. ed$    - look for walked, talked, seed

	(pattern)      - treat as 1 group or specific match
		ex. (bo).$ - look for ends with 
		
	pattern*       - occur 0 or more
		ex. [0-9]*\.txt   - one or more digits with .txt
			- 324.txt, 8.txt, 3243.txt, 6786.txt, 1.txt
	
	pattern{num}   - number of occurence
		ex. pattern{2}  - exactly 2 occurence
		ex. pattern{2,} - two or more occurence

	\              - escape pattern to treat as string
		ex. \\, \*, \', \", \.
		
	|              - or
		ex. 
			\.(txt|py)   - look .txt or .py



	?<=         - positive lookbehind
		ex. 


	?<!         - negative lookbehind
		ex. 

	?=          - positive lookahead
		ex. 


	?!          - negative lookahead
		ex. 
	
	
			
```


- .       - any character 
```python
	ls | egrep "[a-z]\.txt"

	- search for files that has a to z and with .txt
	- e.g. myfile.txt
		   2text.txt
		   firewall rules.txt
```



- multiple pattern using -e
```python
	ls | egrep -e "[a-z]\.txt" -e "[0-9]\.txt"

	- search for [a-z].txt and also [0-9].txt
```
