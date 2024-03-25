
# definition
```python
- this module allows you to work with dates and times
```

### import datetime
```python
import datetime
```

# get date today
```python
import datetime
today = datetime.date.today()
print(today)


# example output is 2023-03-23
```


# date today - month, day, year

```python
import datetime
today = datetime.date.today()
print(today.month)
print(today.day)
print(today.year)

# example output is:
'''
3
23
2023
'''
```



# weekday and isoweekday
- weekday - Monday is 0, Sunday is 6
- isoweekday -  Monday is 1, Sunday is 7
```python
# weekday - Monday is 0, Sunday is 6
import datetime
today = datetime.date.today()
print(today.weekday())
print(today.isoweekday())


# if today is Monday then the output will be:

'''
0
1
'''
```


# timedelta
- used for calculations of date such as differences in date 

```python
import datetime
today = datetime.date.today()
last2Weeks = datetime.timedelta(days=14)
day2WeeksAgo = today - last2Weeks
print(day2WeeksAgo)


```



# calculate remaining days until specific days from today
```python
import datetime
today = datetime.date.today()
theday = datetime.date(2024, 4, 20)
days = (theday - today).days
months = days / 30
print(days)
print(months)
```


# current time - hour:mins:secs:millisecs
```python
import datetime
print(datetime.datetime.now().time())
```



















































