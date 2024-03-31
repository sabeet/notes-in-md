
When an error occurs in Java, it tries to throw an exception

These exceptions can be handled via try-catch blocks

```java
try {
  //  Block of code to try
}
catch(Exception e) {
  //  Block of code to handle errors
}
```

---

You can add a Finally to execute more code regardless of error or not

```java
public class Main {
  public static void main(String[] args) {
    try {
      int[] myNumbers = {1, 2, 3};
      System.out.println(myNumbers[10]);
    } catch (Exception e) {
      System.out.println("Something went wrong.");
    } finally {
      System.out.println("The 'try catch' is finished.");
    }
  }
}

// Something went wrong.  
// The 'try catch' is finished.
```

---
Throws can check for errors directly in the signature of the function/method

```java
public class AgeValidator {

    public static void validate(int age) throws IllegalArgumentException {
        if (age < 0) {
            throw new IllegalArgumentException("Age cannot be negative");
        }
    }
}
```
