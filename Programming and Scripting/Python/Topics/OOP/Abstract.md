- contains one or more abstract methods
- a class should have at least 1 abstract method to implement abstract concept
- all child class who inherit the parent/abstract class should implement the parent/abstract class' abstract method


# Basic
```python
from abc import ABC, abstractmethod

class Animal(ABC):
    @abstractmethod
    def eat(self):
        pass

class Dog(Animal):
    def eat(self):
        print('This dog is eating')

    def bark(self):
        print("Woof!")


dog = Dog()
dog.eat()
dog.bark()


```

































