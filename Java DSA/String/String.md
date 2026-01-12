# Strings in Java

## String
- Strings in Java are immutable, meaning once created, their values cannot be changed.
- Stored in the **String Constant Pool (SCP)** for memory optimization.
- Example:
  ```java
  String s1 = "Hello";
  String s2 = "Hello"; // Points to the same object in SCP
  ```

## String Constant Pool (SCP)
- A special memory area inside the heap where string literals are stored.
- If a string literal already exists in the SCP, a new reference is created instead of allocating new memory.

## StringBuilder
- A mutable sequence of characters.
- Not thread-safe but faster than `StringBuffer`.
- Example:
  ```java
  StringBuilder sb = new StringBuilder("Hello");
  sb.append(" World"); // Modifies the same object
  ```

### Common Functions in StringBuilder
1. **append(String str)**: Appends the specified string to the sequence.
   ```java
   sb.append(" World");
   ```

2. **insert(int offset, String str)**: Inserts the specified string at the given offset.
   ```java
   sb.insert(5, " Java");
   ```

3. **replace(int start, int end, String str)**: Replaces the characters in the specified range with the given string.
   - `start` is inclusive, `end` is exclusive.
   ```java
   sb.replace(0, 5, "Hi");
   ```

4. **delete(int start, int end)**: Removes the characters in the specified range.
   - `start` is inclusive, `end` is exclusive.
   ```java
   sb.delete(0, 3);
   ```

5. **reverse()**: Reverses the sequence of characters.
   ```java
   sb.reverse();
   ```

6. **capacity()**: Returns the current capacity of the `StringBuilder`.
   ```java
   int capacity = sb.capacity();
   ```

7. **charAt(int index)**: Returns the character at the specified index.
   ```java
   char ch = sb.charAt(2);
   ```

8. **length()**: Returns the length of the sequence.
   ```java
   int len = sb.length();
   ```

9. **substring(int start, int end)**: Returns a substring from the specified range.
   - `start` is inclusive, `end` is exclusive.
   ```java
   String sub = sb.substring(0, 5);
   ```

10. **toString()**: Converts the `StringBuilder` object to a `String`.
   ```java
   String str = sb.toString();
   ```

## StringBuffer
- Similar to `StringBuilder` but thread-safe (synchronized).
- Slightly slower than `StringBuilder` due to synchronization overhead.
- Example:
  ```java
  StringBuffer sb = new StringBuffer("Hello");
  sb.append(" World"); // Modifies the same object
  ```

## Key Differences
| Feature          | String       | StringBuilder | StringBuffer |
|------------------|--------------|---------------|--------------|
| Mutability       | Immutable    | Mutable       | Mutable      |
| Thread-Safe      | No           | No            | Yes          |
| Performance      | Fast         | Faster        | Slower       |
