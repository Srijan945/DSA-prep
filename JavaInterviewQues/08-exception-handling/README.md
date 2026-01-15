# Exception Handling — Q&A

91. Why is exception handling important?
- To manage runtime errors, maintain program flow and resource cleanup.

92. What design pattern is used to implement exception handling features in most languages?
- The Chain of Responsibility-like propagation of exceptions up the call stack.

93. What is the need for finally block?
- To run cleanup code regardless of exception occurrence.

94. In what scenarios is code in finally not executed?
- When JVM exits (System.exit) or thread is killed, or catastrophic errors (e.g., power loss).

95. Will finally be executed in the program below?
- Provide code to determine; generally finally executes unless JVM exits.

96. Is try without a catch is allowed?
- Only if try has a finally block (try + finally).

97. Is try without catch and finally allowed?
- No.

98. Can you explain the hierarchy of exception handling classes?
- Throwable -> Error and Exception; Exception -> RuntimeException (unchecked) and checked exceptions.

99. What is the difference between error and exception?
- Errors are serious system problems (not usually handled); exceptions are recoverable conditions.

100. What is the difference between checked exceptions and unchecked exceptions?
- Checked must be caught or declared; unchecked (RuntimeException) need not be.

101. How do you throw an exception from a method?
- Use throw new ExceptionType(...);

102. What happens when you throw a checked exception from a method?
- Must declare it with throws or handle it; otherwise compile-time error.

103. What are the options you have to eliminate compilation errors when handling checked exceptions?
- Catch the exception or declare it in method signature with throws.

104. How do you create a custom exception?
- Extend Exception (checked) or RuntimeException (unchecked) and add constructors.

105. How do you handle multiple exception types with same exception handling block?
- Use multi-catch (catch (A | B e)) or catch a common superclass.

106. Can you explain about try with resources?
- try(resource-declaration) automatically closes resources that implement AutoCloseable.

107. How does try with resources work?
- Resources are closed automatically in reverse order after try block, even on exceptions.

108. Can you explain a few exception handling best practices?
- Prefer specific exceptions, avoid swallowing, clean up resources, document thrown exceptions.
