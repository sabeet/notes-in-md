
---
In Java, Binding refers to the implementation of a method call. Binding can take place either during runtime or compile time

---
# Dynamic Binding 

Dynamic binding, aka Late Binding takes place during runtime

```java
// Dynamic binding example
class Animal {
  public void makeSound() {
    System.out.println("Animal sound");
  }
}

class Dog extends Animal {
  @Override
  public void makeSound() {
    System.out.println("Woof!");
  }
}

public class Main {
  public static void main(String[] args) {
    Animal animal = new Dog();
    animal.makeSound(); // Prints "Woof!"
  }
}
```

The Animal animal object calling on the class Dog. Because Dog inherits from Animal, we are able to do this. This makes the Binding static however.
# Static Binding

Static binding takes place during compile time

```java
// Static binding example
class Animal {
  public void makeSound() {
    System.out.println("Animal sound");
  }
}

class Dog extends Animal {
  @Override
  public void makeSound() {
    System.out.println("Woof!");
  }
}

public class Main {
  public static void main(String[] args) {
    Animal animal = new Animal();
    animal.makeSound(); // Prints "Animal sound"

    Dog dog = new Dog();
    dog.makeSound(); // Prints "Woof!"
  }
}
```

`makeSound()` is statically bounded to the animal class at compile time. We can tell by noticing that `dog.makeSound()` happens but it's because the dog object comes from the line above. `Dog dog = new Dog();`.  Because it is coming from `new Dog()` and not `new Animal()`, that means that the Animal's class implementation wasn't called, which makes this static and not dynamic.