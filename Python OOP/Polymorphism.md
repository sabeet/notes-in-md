
---

Polymorphism means of many forms. This means that a program can have multiple method/function with the same name do different things.

---
# Functional Polymorphism

Python's `len()` function does this. You can get the length of a string, a list, and a dictionary by doing this. The `len()` was designed to handle various objects.

---
# Class Polymorphism

All these classes have a move method. x in the for loop has the ability to run through all of them without specifying the exact class.

```python
class Car:  
  def __init__(self, brand, model):  
    self.brand = brand  
    self.model = model  
  
  def move(self):  
    print("Drive!")  
  
class Boat:  
  def __init__(self, brand, model):  
    self.brand = brand  
    self.model = model  
  
  def move(self):  
    print("Sail!")  
  
class Plane:  
  def __init__(self, brand, model):  
    self.brand = brand  
    self.model = model  
  
  def move(self):  
    print("Fly!")  
  
car1 = Car("Ford", "Mustang")       #Create a Car class  
boat1 = Boat("Ibiza", "Touring 20") #Create a Boat class  
plane1 = Plane("Boeing", "747")     #Create a Plane class  
  
for x in (car1, boat1, plane1):  
  x.move()
```

---
# Inheritance Class Polymorphism

This is like runtime polymorphism from java where you have the ability to override methods. You can create a parent class with a specific method and the child classes can inherit that method and that method may then be overriden.

```python
class Vehicle:  
  def __init__(self, brand, model):  
    self.brand = brand  
    self.model = model  
  
  def move(self):  
    print("Move!")  
  
class Car(Vehicle):  
  pass  
  
class Boat(Vehicle):  
  def move(self):  
    print("Sail!")  
  
class Plane(Vehicle):  
  def move(self):  
    print("Fly!")  
  
car1 = Car("Ford", "Mustang") #Create a Car object  
boat1 = Boat("Ibiza", "Touring 20") #Create a Boat object  
plane1 = Plane("Boeing", "747") #Create a Plane object  
  
for x in (car1, boat1, plane1):  
  print(x.brand)  
  print(x.model)  
  x.move()  
```