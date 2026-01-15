# Java Platform — Q&A

1. Why is Java so popular?
- Cross-platform, rich standard library, strong community, robustness and portability.

2. What is platform independence?
- Write once, run anywhere: compiled bytecode runs on any JVM regardless of OS/hardware.

3. What is bytecode?
- Intermediate, platform-independent binary format produced by the Java compiler; executed by the JVM.

4. Compare JDK vs JVM vs JRE
- JDK: development kit (compiler, tools). JRE: runtime (JVM + core libs). JVM: runtime engine that executes bytecode.

5. What are the important differences between C++ and Java?
- Java: managed memory (GC), no pointers, platform-independent, single inheritance for classes, built-in libraries; C++: manual memory, pointer arithmetic, multiple inheritance, platform-dependent.

6. What is the role for a classloader in Java?
- Loads class bytecode into the JVM, performs linking and initialization; enables dynamic loading and isolation.
