# Modifiers — Q&A

64. What is default class modifier?
- Package-private: accessible within the same package.

65. What is private access modifier?
- Accessible only within the declaring class.

66. What is default or package access modifier?
- No modifier; accessible within same package.

67. What is protected access modifier?
- Accessible in same package and subclasses (even in other packages).

68. What is public access modifier?
- Accessible from any other class.

69. What access types of variables can be accessed from a class in same package?
- public, protected, default, private? (private not accessible). So public, protected, default.

70. What access types of variables can be accessed from a class in different package?
- public only (unless subclass — then protected applies).

71. What access types of variables can be accessed from a sub class in same package?
- public, protected, default (package), not private.

72. What access types of variables can be accessed from a sub class in different package?
- public and protected (protected via inheritance).

73. What is the use of a final modifier on a class?
- Prevents the class from being subclassed.

74. What is the use of a final modifier on a method?
- Prevents overriding.

75. What is a final variable?
- Constant reference/value that cannot be reassigned.

76. What is a final argument?
- Method parameter that cannot be reassigned inside the method.

77. What happens when a variable is marked as volatile?
- Ensures visibility of changes across threads (no caching of the variable in thread-local caches).

78. What is a static variable?
- Class-level variable shared by all instances.
