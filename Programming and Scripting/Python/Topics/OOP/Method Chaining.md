

# Calling method sequentially
```python
class Car:
    def startEngine(self):
        print('start engine')
        return self

    def drive(self):
        print('drive')
        return self

    def stop(self):
        print('stop')
        return self

    def stopEngine(self):
        print('stop engine')
        return self
    
car = Car()
car.startEngine().drive().stop().stopEngine()



```































