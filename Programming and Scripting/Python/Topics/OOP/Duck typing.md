
# Basic
@geeksforgeeks
- Duck Typing is a type system used in dynamic languages. For example, Python, Perl, Ruby, PHP, Javascript, etc. where the type or the class of an object is less important than the method it defines. Using Duck Typing, we do not check types at all. Instead, we check for the presence of a given method or attribute.

The name Duck Typing comes from the phrase:
“If it looks like a duck and quacks like a duck, it’s a duck”

```python
class Dog:
    def makeSound(self):
        print('Woof!')

class Cat:
    def makeSound(self):
        print('Meow!')

def makeSound(animal):
    animal.makeSound()

dog = Dog()
cat = Cat()

makeSound(dog)
makeSound(cat)

```































