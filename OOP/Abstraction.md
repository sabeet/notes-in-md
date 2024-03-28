
---
Abstraction is the process of hiding certain details away and showing essential information to the user. The way it differs from encapsulation is that:

Abstract classes are restricted and cannot be instantiated. To access it, you have to inherit from an abstract class

Abstract method can only be used in an abstract class and body of the method is provided in the subclass

```java
// Abstract class
abstract class Animal {
  // Abstract method (does not have a body)
  public abstract void animalSound();
  // Regular method
  public void sleep() {
    System.out.println("Zzz");
  }
}

// Subclass (inherit from Animal)
class Pig extends Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig(); // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}
```

Abstaction can only be achieved via interfaces
