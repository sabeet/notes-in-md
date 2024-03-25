
Enum is a special class that contains Public Static Final variables. Effectively treat them like constants. These variables can be accessed with dot operator notations.

```java
public class Main {
  enum Level {
    LOW,
    MEDIUM,
    HIGH
  }

  public static void main(String[] args) {
    Level myVar = Level.MEDIUM; 
    System.out.println(myVar);
  }
}

//output: MEDIUM

```
