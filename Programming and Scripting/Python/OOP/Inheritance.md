
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
















