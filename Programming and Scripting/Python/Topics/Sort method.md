
# Note
```python
- it only works with list type of data, use the method/function called "sorted" for all iterable
```



# Basic
```python
numList = [6, 5, 4, 7, 2, 3, 1, 9, 8, 10]
print(numList)
numList.sort()
print('list sorted')
print(numList)
```



# Reverse Sort
```python
numList = [6, 5, 4, 7, 2, 3, 1, 9, 8, 10]
print(numList)
numList.sort()
print('list sorted')
print(numList)
```



# Using a key for multiple data
- the lambda "ages" represents each tuple or data of each student and accessing the 2 index which is the element of the ages using ages[2]
- note that you can only use the sort method on a list, use sorted() instead if other than list 

```python
students = [('mark vince', 'm', 28),
            ('lumen', 'm', 35),
            ('aiden pearce', 'm', 30)]

students.sort(key=lambda ages: ages[2])

for val in students:
    print(val)
```


### Sorted method for other data type other than list
```python
students = (('mark vince', 'm', 28),
            ('lumen', 'm', 35),
            ('aiden pearce', 'm', 30))

students_sorted = sorted(students, key=lambda ages: ages[2])

for val in students_sorted:
    print(val)

```






















