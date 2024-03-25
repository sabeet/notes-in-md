Polymorphism is one of the four pillars of OOP

Poly means many
Morph means form

Because Inheritance let's us pick up attributes of other classes, we can use polymorphism to perform different tasks to improve code reusability.

```java
class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class Pig extends Animal {
  public void animalSound() {
    System.out.println("The pig says: wee wee");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog says: bow wow");
  }
}
```

Pig and Dog rewrites Animals animalSound method

---
<center><h2>There are 4 types of Polymorphism</h2></center>
<center><h2>↓</h2></center>

---
**Coercion Polymorphism :** Occurs when an object or primitive is cast into some other type.

This is just typecasting

---

**Inclusion Polymorphism :** The ability to use derived classes through base class pointers and references. It is also known as Run-time polymorphism

``` java
abstract class Image {
	public Image() {
	}

	abstract void display();
}

class Jpg extends Image {
	public Jpg() {
	}

	@Override
	void display() {
		System.out.println("JPG Image File");
	}
}

class Png extends Image {
	public Png() {
	}

	@Override
	void display() {
		System.out.println("PNG Image File");
	}
}

public class Main {
	public static void main(String[] args) {
		Image img;
		Jpg jg = new Jpg();
		Png pg = new Png();

		// stores the reference of Jpg
		img = jg;

		// invoking display() method of Jpg
		img.display();

		// stores the reference of Png
		img = pg;

		// invoking display() method of Png
		img.display();
	}
}

```

---

**Parametric Polymorphism :** This opens a way to use the same piece of code for different types.

```java
public class GreaterDemo {
	// Generic method to find the greater of two values
	public static <T extends Comparable<T>> T greater(T a, T b) {
		if (a.compareTo(b) > 0) {
			return a;
		} else {
			return b;
		}
	}

	public static void main(String[] args) {
		// Example with integers
		System.out.println(greater(55, 11));

		// Example with strings
		String str1 = "Early";
		String str2 = "Binding";
		System.out.println(greater(str1, str2));
	}
}
```

Use of generics to use functions of the same name to achieve whatever the template of that generics will allow

---

**Ad Hoc Polymorphism :** Allows functions having same name to act differently for different types. AKA [[Overloading]]

```java
import java.util.*;

public class Main {
	public static int sum(int x, int y)
	{
		int c = x + y;
		return c;
	}

	public static String sum(String x, String y)
	{
		String summation = x.concat(y);
		return summation;
	}

	public static void main(String[] args)
	{
		System.out.println(sum(50, 20)
						+ " :- Integer addition Output");
		System.out.println(
			sum("Polymorphism", " achieved")
			+ " :- String Concatenation Output");
	}
}
```

All this just means int sum and string sum have the same name but operate differently. Same name but two different functions