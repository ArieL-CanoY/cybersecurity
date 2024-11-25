### What is Numpy
```
Numpy stands for Numerical Python use to work with arrays and more faster that Python's built in array/list
```


Array Creation And Accessing
```python
import numpy as np

arr_0d = np.array(28)  # 0D array
arr_1d = np.array([1,2,3])  # 1D array
print(arr_1d[1])  # 2
arr_2d = np.array([[1,2,3],[4,5,6]])  # 2D array
print(arr_2d[1,2])  # 6
arr_3d = np.array([[[1,2,3],[1,2,3]],[[1,2,3],[1,2,3]]])  # 3D array
print(arr_3d[0,0,0])  # 1
```


Array information
```python
import numpy as np

arr = np.array([[1, 2, 3], [4, 5, 6]])
print(arr.shape)  # dimension - rows(list) and columns(items within list) - output is ()
print(arr.size)  # number of individual items - output is 6
print(arr.ndim)  # number of rows or dimentional (n dimentional) - output is 2
```


Appending array
```python
import numpy as np

arr1 = np.array([1, 2, 3])
arr2 = np.array([4, 5, 6])

combineResult = numpy.append(arr1, arr2)
print(combineResult)
```


zero shape - make all the rows and columns a value of zero
```python
import numpy as np

zeroShape = np.zeros((5,5))  # zeroes as float numbers
zeroShape = np.zeros((5,5), dtype=int)  # zeroes as integer numbers
```


one shape - make all the rows and columns a value of one
```python
import numpy as np

zeroShape = np.ones((5,5))  # zeroes as float numbers
zeroShape = np.ones((5,5), dtype=int)  # zeroes as integer numbers
```


range array - similar to Python range
```python
import numpy as np

rangeArr = np.arange(5)
print(rangeArr)  # [0 1 2 3 4]

rangeArr = np.arange(2, 7, 2)
print(rangeArr)  # [2 4 6]




```




linspace - (start, stop_include, numbers_to_generate_between_start_and_stop)
```python
import numpy as np

min = 5
max = 15
division = 5
divideArr = np.linspace(min, max, division)
print(divideArr)  # [ 5.   7.5 10.  12.5 15. ]



min = 5
max = 15
division = 3
divideArr = np.linspace(min, max, division)
print(divideArr)  # [ 5. 10. 15.]


# the formula is "print( (max-min) / (division-1) )"



```




Just like np.zeroes and np.ones, it will fill up based on the number provided


```python
import numpy as np

arr = np.full((3, 3), 0)
print(arr)

'''
output is 

[[0 0 0]
 [0 0 0]
 [0 0 0]]
'''

```



np.eye(num)
```python
import numpy as np

arr = np.eye(5)
print(arr)


'''
output is 

[[1. 0. 0. 0. 0.]
 [0. 1. 0. 0. 0.]
 [0. 0. 1. 0. 0.]
 [0. 0. 0. 1. 0.]
 [0. 0. 0. 0. 1.]]
'''


```



reshape - change the rows and columns values
```python
import numpy as np

arr = np.array([[1,2,3], [4,5,6]])
print(arr)
print()
arr = arr.reshape((3,2))
print(arr)



'''
output is 

[[1 2 3]
 [4 5 6]]

[[1 2]
 [3 4]
 [5 6]

'''
```



condition to change the value 
```python
import numpy as np

arr = np.array([[1,2,3], [4,5,6], [7,8,9]])
print(arr)
print()
arr[arr == 5] = 45  # if the value is 5 then change it to 45
print(arr)



'''
output is 

[[1 2 3]
 [4 5 6]
 [7 8 9]]

[[ 1  2  3]
 [ 4 45  6]
 [ 7  8  9]

'''

# note that you can condition other cases like greater or less than, etc.

```



change all the value of specific row
```python
import numpy as np

arr = np.array([[1,2,3], [4,5,6], [7,8,9]])
print(arr)
print()
arr[0] = 3
print(arr)

'''
output is:
[[1 2 3]
 [4 5 6]
 [7 8 9]]

[[3 3 3]
 [4 5 6]
 [7 8 9]]
'''


# note that you can slice it like arr[:2] = 3, this will select the first up to second row to change all the value to 3


```


change specific rows and column
```python
import numpy as np

arr = np.array([[1,2,3], [4,5,6], [7,8,9]])
print(arr)
print()
arr[:2, 2] = 3
print(arr)

```




change specific list of rows and columns
```python
import numpy as np

arr = np.array([[1,2,3], [4,5,6], [7,8,9]])
print(arr)
print()
arr[[0,2], [0, -1]] = 3  # the first list is [0, 2] which is the first and third rows, the second list is [0, -1] which is the first and last columns, which if combined, it will become the (first row, first column), and the (third row, last column)
print(arr)


'''
output is:

[[1 2 3]
 [4 5 6]
 [7 8 9]]

[[3 2 3]
 [4 5 6]
 [7 8 3]]

'''
```






sort every row
```python
import numpy as np

arr = np.array([[8,3,6], [1,7,4], [9,5,2]])
print(arr)
print()
print(np.sort(arr))

'''
output is:

[[8 3 6]
 [1 7 4]
 [9 5 2]]

[[3 6 8]
 [1 4 7]
 [2 5 9]]
'''

```




sort every column
```python
import numpy as np

arr = np.array([[8,3,6], [1,7,4], [9,5,2]])
print(arr)
print()
print(np.sort(arr, axis=0))  # axis default is -1


'''
output is:

[[8 3 6]
 [1 7 4]
 [9 5 2]]

[[1 3 2]
 [8 5 4]
 [9 7 6]]
 '''

# read every column downward, 1 8 9, 3 5 6, 2 4 6

```



kinds of sorting algorithm
```python
import numpy as np

# you can pass different kinds of sorting algorithm
print(np.sort(arr, axis=-1, kind='heapsort'))
```



copy the array

```python
import numpy as np

arr = np.array([[8,3,6], [1,7,4], [9,5,2]])
copyArr = arr.view()
copyArr2 = arr.copy()

```




