# Object Oriented Programming Basics — Q&A

23. What is a class?
- A blueprint defining state (fields) and behavior (methods).

24. What is an object?
- An instance of a class with specific state.

25. What is state of an object?
- Values of its fields at a given time.

26. What is behavior of an object?
- Methods/actions the object can perform.

27. What is the super class of every class in Java?
- java.lang.Object.

28. Explain about toString method ?
- Returns string representation; override to provide meaningful output.

29. What is the use of equals method in Java?
- To compare object logical equality (override to define equality).

30. What are the important things to consider when implementing equals method?
- Reflexive, symmetric, transitive, consistent and null-handling; check instanceof and compare significant fields.

31. What is the Hashcode method used for in Java?
- Returns an int used in hashing structures; equal objects must have same hashCode.

32. Explain inheritance with examples .
- A class can extend another to reuse fields/methods (e.g., class Dog extends Animal).

33. What is method overloading?
- Multiple methods with same name but different parameter lists in same class.

34. What is method overriding?
- Subclass provides specific implementation for a superclass method with same signature.

35. Can super class reference variable can hold an object of sub class?
- Yes (polymorphism).

36. Is multiple inheritance allowed in Java?
- Not for classes; multiple interfaces can be implemented.

37. What is an interface?
- A contract with abstract methods and static/default implementations (since Java 8).

38. How do you define an interface?
- Use the interface keyword and declare methods/constants.

39. How do you implement an interface?
- A class uses implements and provides method implementations.

40. Can you explain a few tricky things about interfaces?
- Default and static methods allowed; fields are public static final; multiple inheritance of defaults can cause conflicts.

41. Can you extend an interface?
- Yes, interfaces can extend other interfaces.

42. Can a class extend multiple interfaces?
- A class implements multiple interfaces (extends keyword is for classes).

43. What is an abstract class?
- A class with abstract methods; cannot be instantiated directly.

44. When do you use an abstract class?
- When sharing code among related classes and defining some abstract behavior.

45. How do you define an abstract method?
- Use abstract keyword in method signature inside an abstract class.

46. Compare abstract class vs interface?
- Abstract class can have state and constructors; interfaces are primarily contracts (modern interfaces can have defaults/static).

47. What is a constructor?
- Special method to initialize new objects.

48. What is a default constructor?
- No-arg constructor provided by compiler when none declared.

49. Will this code compile?
- (Insufficient context) Provide code to answer. Please add the file or code snippet if you want compilation check.

50. How do you call a super class constructor from a constructor?
- Using super(...) as the first statement in subclass constructor.

51. Will this code compile?
- (Insufficient context) Provide code to answer.

52. What is the use of this()?
- Calls another constructor in the same class (constructor chaining); must be first statement.

53. Can a constructor be called directly from a method?
- No; constructors are invoked with new or via this()/super() inside constructors.

54. Is a super class constructor called even when there is no explicit call from a sub class constructor?
- Yes; the default no-arg super() is invoked automatically if present.
