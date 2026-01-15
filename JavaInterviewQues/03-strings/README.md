# Strings — Q&A

16. Are all String’s immutable?
- Yes; String objects are immutable.

17. Where are String values stored in memory?
- In the String pool (interned) and heap; literal strings go to the pool.

18. Why should you be careful about String concatenation(+) operator in loops?
- It creates many intermediate immutable objects, causing performance overhead.

19. How do you solve above problem?
- Use StringBuilder or StringBuffer (for thread-safety) to accumulate strings.

20. What are differences between String and StringBuffer?
- String immutable; StringBuffer mutable and synchronized (thread-safe).

21. What are differences between StringBuilder and StringBuffer?
- Both mutable; StringBuilder is unsynchronized (faster), StringBuffer is synchronized.

22. Can you give examples of different utility methods in String class?
- length(), substring(), indexOf(), equals(), equalsIgnoreCase(), split(), trim(), replace(), toLowerCase(), toUpperCase(), contains().
