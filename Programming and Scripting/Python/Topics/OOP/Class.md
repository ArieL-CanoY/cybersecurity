


# Basic 
```python
class User:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        print(f'I am {self.name} and I am {self.age} years old.')


user = User('Mark Vince', 28)

print(user.name)
print(user.age)
user.introduce()

```



# Class and Instance Variable
```python
class Car:
    wheels = 4  # class variable
    
    def __init__(self, make, model, year, color):
        self.make = make  # instance variable
        self.model = model  # instance variable
        self.year = year  # instance variable
        self.color = color  # instance variable



```






























