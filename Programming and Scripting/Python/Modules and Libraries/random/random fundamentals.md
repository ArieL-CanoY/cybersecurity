### import random
```python
import random as <alias>
```


### random int with range
```python
# print a random between 1 and 10

randoNum = rand.randint(1,10)
print(randoNum)
```


### random int like range
```python
# print a random between 1 and 9, not including 10

randoNum = rand.randint(1,10)
print(randoNum)
```


### random choice 
```python
# choose a random from the list of names

import random as rand
names = ['mark', 'vince', 'lumen']
randomName = rand.choice(names)
print(randomName)
```


### shuffle a list
```python
# it will shuffle the list and it returns None

import random as rand
cards = list(range(1,53))
rand.shuffle(cards)
print(cards)
```


### get a sample 
```python
# randomly pick 2 numbers and put it in a list

import random as rand
numList = range(10)
numToPick = 2
sampleData = rand.sample(numList, numToPick)
print(sampleData)
```


### random float range
```python

import random as rand
randomFloat = rand.uniform(60, 98)
randomFloat = round(randomFloat, 2)
print(randomFloat)

```






















