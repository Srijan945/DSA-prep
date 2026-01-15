# Generics — Q&A

178. What are Generics?
- Language feature to parameterize types (e.g., List<String>) for type safety.

179. Why do we need Generics? Can you give an example of how Generics make a program more flexible?
- Provide compile-time type checking and remove casts; e.g., List<String> prevents adding non-String.

180. How do you declare a generic class?
- class Box<T> { private T value; }

181. What are the restrictions in using generic type that is declared in a class declaration?
- Cannot use primitive types directly, cannot create generic arrays, type erasure prevents certain runtime type checks.

182. How can we restrict Generics to a subclass of particular class?
- Use extends bound: <T extends Number>.

183. How can we restrict Generics to a super class of particular class?
- Use super wildcard for method parameters: <? super Integer>.

184. Can you give an example of a generic method?
- public static <T> void swap(T[] arr, int i, int j) { ... }
