
# Basic
- Dog and Fish inherit the attribute "canEat" of the Animal class

```python
class Animal():
    canEat = True

    def eat(self):
        print(f'Eating is {self.canEat}')

class Dog(Animal):
    def walk(self):
        print("dog walking")

class Fish(Animal):
    def swim(self):
        print("fish swimming")




dog = Dog()
fish = Fish()

dog.walk()
dog.eat()
fish.swim()
fish.eat()

```



# With constructor
- Dog inherit Animal class with constructor(def \_\_init\_\_)  with argument "type", therefore, when creating a class of Dog, it is required to enter its type
```python
class Animal():
    isAlive = True

    def __init__(self, type):
        self.type = type


class Dog(Animal):
    isBiting = True
    def bark(self):
        print("Woof!")

dog = Dog('Land Animal')
print(dog.type)
print(dog.isAlive)
dog.bark()
print(dog.isBiting)

```



# Multiple Constructor set
```python
class Prey():
    def __init__(self, preyType):
        self.preyType = preyType

    def hide(self):
        print('Hide for life')

class Predator():
    def __init__(self, predatorType):
        self.predatorType = predatorType

    def hunt(self):
        print('Hunt for life')

class Snake(Prey, Predator):

    def __init__(self, preyType, predatorType):
        Prey.__init__(self, preyType)
        Predator.__init__(self, predatorType)
    def eat(self):
        print('I want to eat')


snake = Snake('python', 'cobra')
snake.eat()
print(snake.preyType)
print(snake.predatorType)

```




# Multi-Level Inheritance
- Dog inherit the walk of LandAnimal
- LandAnimal inherit the attribute "canEat" of Animal
- Therefore, Dog inherit also the attribute "canEat" of Animal

```python
class Animal():
    canEat = True

class LandAnimal(Animal):
    def walk(self):
        print("walk")

class Dog(LandAnimal):
    def bark(self):
        print("bark")


landAnimal = LandAnimal()
dog = Dog()

dog.bark()
dog.walk()
print(dog.canEat)
landAnimal.walk()

```



# Multiple Inheritance
- Snake class inherit both Prey and Predator class' function

```python
class Prey():
    def hide(self):
        print('Hide for life')

class Predator():
    def hunt(self):
        print('Hunt for life')


class Snake(Prey, Predator):
    def eat(self):
        print('I want to eat')

snake = Snake()
snake.hide()
snake.eat()
snake.hunt()



```






# super() function
```python
class Animal():
    def __init__(self, name):
        self.name = name

class Dog(Animal):
    def __init__(self, name):
        super().__init__(name)

dog = Dog('Mark')
print(dog.name)

```









