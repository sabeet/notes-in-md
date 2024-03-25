
---
Python lets a class derive object attributes from another class. The parent class is where the child class can get it's attributes from

```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    return f"{self.firstname} {self.lastname}"

class Student(Person):
  pass

x = Student("Adam", "Ali")
print("My name is", x.printname(), "and I am a",  x.__class__.__name__)

y = Person("Raheem", "Zakaria")
print("My name is", y.printname(), "and I am a",  y.__class__.__name__)

#output: My name is Adam Ali and I am a Student
#output: My name is Raheem Zakaria and I am a Person
```

The Student() class takes in the Person() class within its parameter, therefor causing inheritance.
A student is be a person

---
# `super()`

We use `super()` to refer to the base class.

```python
class Mammal(object):
  def __init__(self, mammalName):
    print(mammalName, 'is a warm-blooded animal.')
    
class Dog(Mammal):
  def __init__(self):
    print('Dog has four legs.')
    super().__init__('Dog')
    
d1 = Dog()

#output: Dog has four legs.
#output: Dog is a warm-blooded animal.
```

---
# Multiple Inheritance

Here's an example of multiple inheritance,

```python
class Animal:
  def __init__(self, Animal):
    print(Animal, 'is an animal.');

class Mammal(Animal):
  def __init__(self, mammalName):
    print(mammalName, 'is a warm-blooded animal.')
    super().__init__(mammalName)
    
class NonWingedMammal(Mammal):
  def __init__(self, NonWingedMammal):
    print(NonWingedMammal, "can't fly.")
    super().__init__(NonWingedMammal)

class NonMarineMammal(Mammal):
  def __init__(self, NonMarineMammal):
    print(NonMarineMammal, "can't swim.")
    super().__init__(NonMarineMammal)

class Dog(NonMarineMammal, NonWingedMammal):
  def __init__(self):
    print('Dog has 4 legs.');
    super().__init__('Dog')
    
d = Dog()
print('')
bat = NonMarineMammal('Bat')

""" Ouput:

Dog has 4 legs.
Dog can't swim.
Dog can't fly.
Dog is a warm-blooded animal.
Dog is an animal.

Bat can't swim.
Bat is a warm-blooded animal.
Bat is an animal.
"""

```



