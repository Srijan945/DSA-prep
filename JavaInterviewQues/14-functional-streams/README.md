# Functional Programming & Streams — Q&A

208. What is functional programming?
- Description: A programming paradigm that treats computation as the evaluation of mathematical functions, emphasizes immutability, pure functions (no side-effects), and functions as first-class citizens.
- Example (Java):
```java
Function<Integer, Integer> square = x -> x * x;
int result = square.apply(5); // 25
```

209. Can you give an example of functional programming?
- Description: Use higher-order functions to transform data instead of mutable loops.
- Example (Java streams):
```java
List<Integer> nums = List.of(1, 2, 3);
List<Integer> squares = nums.stream()
    .map(x -> x * x)
    .collect(Collectors.toList()); // [1,4,9]
```

210. What is a stream?
- Description: An abstraction for processing a sequence of elements supporting aggregate operations. Streams are lazy and can be parallelized.
- Example:
```java
Stream.of(1,2,3).filter(n -> n > 1).forEach(System.out::println);
```

211. Explain about streams with an example?
- Description: Streams enable pipeline processing via intermediate and terminal operations. Intermediate ops are lazy; terminal ops trigger computation.
- Example:
```java
List<Integer> doubled = List.of(-1, 0, 2, 3).stream()
    .filter(x -> x > 0)     // intermediate
    .map(x -> x * 2)        // intermediate
    .collect(Collectors.toList()); // terminal -> [4,6]
```
- What are intermediate operations in streams?
- Answer: Operations like filter, map, distinct which return a Stream and are lazy (deferred until terminal op).

212. What are terminal operations in streams?
- Description: Operations that produce a result or side-effect and trigger the evaluation of the pipeline.
- Examples: collect, forEach, reduce, count.
- Example:
```java
long count = Stream.of(1,2,3,4).filter(n -> n%2==0).count(); // 2
```

213. What are method references?
- Description: Shorthand to refer to methods or constructors using ::. They are concise equivalents to simple lambda expressions.
- Examples:
```java
List<String> names = List.of("a", "bb", "ccc");
names.forEach(System.out::println); // instance method reference
Function<String, Integer> len = String::length; // class::instanceMethod
```

214. What are lambda expressions?
- Description: Anonymous function expressions that can be passed around; syntax: (params) -> body.
- Example:
```java
Predicate<Integer> isEven = x -> x % 2 == 0;
boolean check = isEven.test(4); // true
```

215. Can you give an example of lambda expression?
- Example:
```java
BiFunction<Integer, Integer, Integer> add = (x, y) -> x + y;
int sum = add.apply(2, 3); // 5
```

216. Can you explain the relationship between lambda expressions and functional interfaces?
- Description: Lambdas provide implementations for functional interfaces (interfaces with a single abstract method). The compiler infers the target type.
- Example:
```java
Runnable r = () -> System.out.println("run"); // Runnable is a functional interface
```

217. What is a predicate?
- Description: A functional interface that accepts one argument and returns a boolean. Used for conditional testing.
- Example:
```java
Predicate<String> empty = String::isEmpty;
boolean b = empty.test(""); // true
```

218. What is the functional interface - function?
- Description: Function<T,R> represents a function that accepts a T and returns an R. Useful for mapping/transformation.
- Example:
```java
Function<String, Integer> parse = Integer::parseInt;
int v = parse.apply("42"); // 42
```

219. What is a consumer?
- Description: Consumer<T> accepts a T and performs side-effects (returns void).
- Example:
```java
Consumer<String> printer = System.out::println;
printer.accept("hello"); // prints "hello"
```

220. Can you give examples of functional interfaces with multiple arguments?
- Description: Java provides BiFunction, BiConsumer, BinaryOperator for two-argument operations.
- Examples:
```java
BiFunction<Integer, Integer, Integer> mul = (a,b) -> a * b;
BiConsumer<String, Integer> pairPrinter = (s, i) -> System.out.println(s + ":" + i);
BinaryOperator<Integer> max = Integer::max;
```
