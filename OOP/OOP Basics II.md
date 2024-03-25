Static vs Public

---

When you create a static method, you can actually just write down the function call without having to construct an object for it

```java
  static void myStaticMethod() {
    System.out.println("Static methods can be called without creating objects");
  }
```


```java
myStaticMethod(); // Call the static method
    // myPublicMethod(); This would compile an error
```



---

When you create a public method, you must create an object to be then able to utilize that function call

```java
public void myPublicMethod() {
    System.out.println("Public methods must be called by creating objects");
  }
```


```java
    Main myObj = new Main(); // Create an object of Main
    myObj.myPublicMethod(); // Call the public method on the object
```