
**Access Modifiers**

---

For Classes,

Public : Accessible by all the other classes
Default : Accessible by all the other classes within the same package. Doesn't need to be specified

---

For Methods,

Public : Accessible for all classes
Private : Only Accessible within the main class
Default : Only accessible within the same package. Doesn't need to specified
Protected : Only accessible within the same package and subclasses

---

**Non-Access Modifiers**

---

For classes,

final : Cannot be inherited by other classes
abstract : Cannot be used to create objects

---

For methods,

final : methods cannot be overridden/modified. You wouldn't wanna modify PI right?
static : attributes belong to class rather than objects. You can modify it without having to call a constructor
abstract: Abstract method is provided by the abstract class but the body is in the subclass