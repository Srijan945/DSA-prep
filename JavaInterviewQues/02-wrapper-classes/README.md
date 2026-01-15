# Wrapper Classes — Q&A

7. What are Wrapper classes?
- Object representations of Java primitive types (e.g., Integer, Double).

8. Why do we need Wrapper classes in Java?
- To use primitives where objects are required (collections, generics, APIs).

9. What are the different ways of creating Wrapper class instances?
- Using constructors (deprecated for some types), valueOf(), parseXxx(), and autoboxing.

10. What are differences in the two ways of creating Wrapper classes?
- Constructors always create new objects; valueOf may cache (e.g., Integer.valueOf) and is preferred.

11. What is auto boxing?
- Automatic conversion from primitive to corresponding wrapper object.

12. What are the advantages of auto boxing?
- Cleaner code, easier use with collections/APIs expecting objects.

13. What is casting?
- Converting a value from one type to another.

14. What is implicit casting?
- Automatic widening conversion (e.g., int to long).

15. What is explicit casting?
- Narrowing conversion that must be forced by the programmer (e.g., long to int).
