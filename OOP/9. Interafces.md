
---
Interfaces are used to `implement` abstract classes. As abstract classes have empty bodies for their methods, interfaces can be used to group them.

To access the interface methods, you must use the implements method

```java
// Interface
interface Animal {
  public void animalSound(); // interface method (does not have a body)
  public void sleep(); // interface method (does not have a body)
}

// Pig "implements" the Animal interface
class Pig implements Animal {
  public void animalSound() {
    // The body of animalSound() is provided here
    System.out.println("The pig says: wee wee");
  }
  public void sleep() {
    // The body of sleep() is provided here
    System.out.println("Zzz");
  }
}

class Main {
  public static void main(String[] args) {
    Pig myPig = new Pig();  // Create a Pig object
    myPig.animalSound();
    myPig.sleep();
  }
}
```

- Interfaces cannot be used to create objects. In this case, you can't create Animal
- All methods of interfaces must be overriden
- interface attributes are always final, static, and public
- interface methods are abstract and public
- interface cannot contain a constructor
---
Why do we use Interfaces?

To hide certain details in order to improve security
To achieve multiple inheritance because this cannot be done via Inheritance
