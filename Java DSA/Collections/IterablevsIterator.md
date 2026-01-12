# Iterable vs Iterator (Java) — Brief

Summary:
- Iterable and Iterator are both interfaces Collections Framework.
- Iterable is implemented by a collection-like type to provide an Iterator.
- Iterator is used to traverse elements of a collection.

Key differences:
- Purpose:
  - Iterable<T>: a provider of Iterator<T>. Has a single method iterator() (plus default forEach and spliterator since Java 8).
  - Iterator<T>: a cursor to traverse elements. Methods: hasNext(), next(), remove() (optional), and forEachRemaining().
  ```java
  public interface Iterable {
  ...
  abstract Iterator<T> iterator(); //Returns an 'Iterator'(not iterator) over elements of type T.
  ...
  }
	public interface Iterator {
	...
	abstract boolean hasNext(); //Returns true if the iteration has more elements.
	abstract E next();          //Returns the next element in the iteration.
	...
	}
  ```
- Usage:
  - Iterable enables the enhanced-for (`for (T t : iterable)`) and the forEach method.
  - Iterator gives explicit control over traversal, including safe removal during iteration.

Short examples

- Iterable example (custom collection used with for-each):
```java
import java.util.ArrayList;
import java.util.List;

public class BasicExample {
    public static void main(String[] args) {
        List<String> fruits = new ArrayList<>();
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Cherry");

        // 1. Using Enhanced For-Loop (Targeting the Iterable)
        for (String fruit : fruits) {
            System.out.println(fruit);
        }

        // 2. Using the forEach() default method (Java 8+)
        fruits.forEach(System.out::println);
    }
}
```

- Iterator example (manual traversal and removal):
```java
import java.util.Iterator;
// ... (using the fruits list from above)
Iterator<String> iterator = fruits.iterator();

while (iterator.hasNext()) {
    String fruit = iterator.next();
    System.out.println(fruit);
    
    // Iterators allow safe removal during traversal, unlike for-each loops
    if (fruit.equals("Banana")) {
        iterator.remove(); 
    }
}
```

- Custom Implementation
```java
import java.util.Iterator;
import java.util.List;
import java.util.Arrays;

// A custom class representing a Classroom that can be iterated to see students
class Classroom implements Iterable<String> {
    private List<String> students = Arrays.asList("Alice", "Bob", "Charlie");

    @Override
    public Iterator<String> iterator() {
        // Return the iterator of the internal list
        return students.iterator();
    }
}

public class CustomExample {
    public static void main(String[] args) {
        Classroom myClass = new Classroom();

        // Now we can use our custom object in a for-each loop!
        for (String student : myClass) {
            System.out.println("Student: " + student);
        }
    }
}
```
When to use which
- Implement Iterable when you design a collection-like class and want to support enhanced-for and stream/forEach usage.
- Use Iterator when you need explicit, step-by-step control of traversal (e.g., conditional removal, peek-next patterns).
- Prefer for-each / streams for simple read-only traversals; use Iterator for mutation during traversal or fine-grained control.

Notes
- Java 8 added default Iterable.forEach and spliterator(); Iterator has forEachRemaining().
- remove() on Iterator is optional and may throw UnsupportedOperationException if not supported.
- Iterators from concurrent collections may not throw ConcurrentModificationException and have weaker consistency guarantees.
