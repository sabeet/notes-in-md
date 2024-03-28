
---
# Constructor
---
A **constructor**  is a special method used in java to initialize objects upon creation. It can be used to set values for object attributes

---


```java
// Create a Main class
public class Main {
  int x;  // Create a class attribute

  // Create a class constructor for the Main class
  public Main() {
    x = 5;  // Set the initial value for the class attribute x
  }

  public static void main(String[] args) {
    Main myObj = new Main(); // Create an object of class Main (This will call the constructor)
    System.out.println(myObj.x); // Print the value of x
  }
}

// Outputs 5
```

**Requirements:**
- A constructor must match the class name
- A constructor has no return type
- All classes have a default constructor which means java makes a default one even if you don't


Note: You can also have the Constructor take in parameters
```java
public class Main {
  int x;

  public Main(int y) {
    x = y;
  }

  public static void main(String[] args) {
    Main myObj = new Main(5);
    System.out.println(myObj.x);
  }
}

// Outputs 5
```