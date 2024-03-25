**Inheritance** is one of the four pillars of OOP

In Java, classes have the ability to inherit properties from other classes

**subclass:** This class will inherit properties from another class
**superclass:** This class is what the subclass will inherit its properties from

Inheritance uses the **extends** keyword:

```java
class Vehicle {
  protected String brand = "Ford";        // Vehicle attribute
  public void honk() {                    // Vehicle method
    System.out.println("Tuut, tuut!");
  }
}

class Car extends Vehicle {
  private String modelName = "Mustang";    // Car attribute
  public static void main(String[] args) {

    // Create a myCar object
    Car myCar = new Car();

    // Call the honk() method (from the Vehicle class) on the myCar object
    myCar.honk();

    // Display the value of the brand attribute (from the Vehicle class) and the value of the modelName from the Car class
    System.out.println(myCar.brand + " " + myCar.modelName);
  }
}
```

Notice how Car extends Vehicle
Notice how Child extends Parent

---
Super is used to refer to the parent class

Super will call for the superclass method

```java
// super keyword in java example 
  
// superclass Person 
class Person { 
    void message() { 
        System.out.println("This is person class\n"); 
    } 
} 
// Subclass Student 
class Student extends Person { 
    void message() { 
        System.out.println("This is student class"); 
    } 
    // Note that display() is 
    // only in Student class 
    void display() { 
        // will invoke or call current 
        // class message() method 
        message(); 
  
        // will invoke or call parent 
        // class message() method 
        super.message(); 
    } 
} 
// Driver Program 
class Test { 
    public static void main(String args[]) { 
        Student s = new Student(); 
  
        // calling display() of Student 
        s.display(); 
    } 
}

// Output: This is student class
// Output: This is person class
```

Super will call for the superclass constructor

```java
// Java Code to show use of 
// super keyword with constructor 

// superclass Person 
class Person { 
	Person() { 
		System.out.println("Person class Constructor"); 
	} 
} 
// subclass Student extending the Person class 
class Student extends Person { 
	Student() { 
		// invoke or call parent class constructor 
		super(); 

		System.out.println("Student class Constructor"); 
	} 
} 
// Driver Program 
class Test { 
	public static void main(String[] args) { 
		Student s = new Student(); 
	} 
}

```

They both look kinda similar however, 
the method uses a dot operator(super.)
and the constructor just uses super()