
---
# Encapsulation

Encapsulations is one of the four pillars of OOP.

It allows for the hiding  of data by wrapping them up into units such as a class. It provides security to data members by making variables private and then creating public getter and setter methods to access these variables

---
# Getters And Setters

When a class has an attribute that is private, we can use getter methods to access those values.

When a class has an attribute that is private, we can use setter methods to modify those values

```java
class Person(){
	private String name;

	//getter
	public String getName(){
		return name;
	}

	public void setName(String newName){
		this.name = newName;
	}
}
```

`this` helps us to refer to name from `private String name;`

---
