

---
# Basics :

Classes in python are the templates we use to create instances of that class or objects

```python
class smth:
	x = 5

# instantiate the object
myObj = smth()
print(myObj.x)

# output: 5 

```

---
# `__init__()` :

The `__init__()` function is the constructor for classes. We can use this to assign values to object properties

```python
class Person:  
  def __init__(self, name, age):  
    self.name = name  
    self.age = age  
  
p1 = Person("John", 36)  
  
print(p1.name)  
print(p1.age)

# output: John
# output: 36
```

---
# Object Methods :

Just like Java, Objects can contain methods. we can use `self` in order to refer to current instance's variable to assign values

```python
class Person:  
  def __init__(self, name, age):  
    self.name = name  
    self.age = age  
  
  def myfunc(self):  
    print("Hello my name is " + self.name)  
  
p1 = Person("John", 36)  
p1.myfunc()

# output: Hello my name is John
```

You also don't have to use `self`. Could be anything else

```python
  def myfunc(eggs):  
    print("Hello my name is " + eggs.name)  
```

---
# Modify, Delete, Pass

To modify the properties of an object,

```python
myObj.age = 29
```
 `
to delete an object property,

```python
del myObj.age
```

to delete the entire obj,

```python
del myObj
```

classes cannot be empty to we use pass to avoid that error. Pass is a null operation

```python
class smth:
	pass
```