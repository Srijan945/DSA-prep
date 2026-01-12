# Low-Level Design (LLD)

## Java Interfaces vs Abstract Classes

| Feature | Interface | Abstract Class |
|---|---:|---:|
| Purpose | Define a contract (what) for implementors | Provide partial implementation + contract (what + some how) |
| Multiple inheritance | Yes — a class can implement multiple interfaces | No — a class can extend only one abstract class |
| Method implementation | Since Java 8: default & static methods allowed; before Java 8: none | Can have concrete and abstract methods |
| Fields / State | Only static final (constants) allowed | Can have instance fields (state) |
| Constructors | No constructors (cannot be instantiated) | Can have constructors (for subclass initialization) |
| Access modifiers for methods | public (implicitly) / default methods can be non-public since Java 9 (private allowed) | Can use any access modifier (public/protected/private) |
