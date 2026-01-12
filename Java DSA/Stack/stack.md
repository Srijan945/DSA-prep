# Stack in Java

A **Stack** is a linear data structure that follows the **LIFO (Last In, First Out)** principle. Java provides a built-in `Stack` class in the `java.util` package.

## Commonly Used Methods in `Stack`

1. **push(E item)**  
   Adds an item to the top of the stack.  
   Example: `stack.push(10);`

2. **pop()**  
   Removes and returns the item at the top of the stack. Throws `EmptyStackException` if the stack is empty.  
   Example: `int top = stack.pop();`

3. **peek()**  
   Returns the item at the top of the stack without removing it. Throws `EmptyStackException` if the stack is empty.  
   Example: `int top = stack.peek();`

4. **isEmpty()**  
   Checks if the stack is empty. Returns `true` if the stack is empty, otherwise `false`.  
   Example: `boolean empty = stack.isEmpty();`

5. **search(Object o)**  
   Returns the 1-based position of the object in the stack. Returns `-1` if the object is not found.  
   Example: `int position = stack.search(10);`

## Example Usage

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();

        // Push elements
        stack.push(1);
        stack.push(2);
        stack.push(3);

        // Peek top element
        System.out.println("Top element: " + stack.peek());

        // Pop elements
        System.out.println("Popped: " + stack.pop());

        // Check if stack is empty
        System.out.println("Is stack empty? " + stack.isEmpty());
    }
}
```
