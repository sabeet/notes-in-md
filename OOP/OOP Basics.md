
---
Classes are the templates for objects
Objects are the instances of classes

---
This code will not compile as x in the last SysOut cannot reach x in the Main class

```java
public class Main {
  int x = 10;

  public static void main(String[] args) {
    Main myObj = new Main();
    myObj.x = 25; // x is now 25
    System.out.println(myObj.x);
    System.out.println(x);
  }
}
```

---
However adding public static to the int x increases the scope and when this compiles, both x and myObj.x have a value of 25. Which means myObj.x assigning a new value changes the value in int x = 10 to int x = 25

```java
public class Main {
  int x = 10;

  public static void main(String[] args) {
    Main myObj = new Main();
    myObj.x = 25; // x is now 25
    System.out.println(myObj.x);
    System.out.println(x);
  }
}
```