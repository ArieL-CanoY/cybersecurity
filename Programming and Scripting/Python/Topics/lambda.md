
# Definition
```python
- has any number of parameters but only one (1) expression
- used for small function for a short period of time
- also called as anonymous function
```



# Basic
```python
# structure
lambda (parameters): (expression)
(lambda_name) = lambda (parameters) : (expression)



# no return
add = lambda num1, num2: print(num1 + num2)
add(1, 2)



# with return
add = lambda num1, num2: num1 + num2
result = add(1, 2)
print(result)



# validation
age_check = lambda age: age >= 18
print(age_check(12))



# ternary
age_check = lambda age: True if age >= 18 else False
print(age_check(12))
```






























