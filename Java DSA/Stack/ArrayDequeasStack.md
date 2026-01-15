# Using ArrayDeque as Stack and Queue

ArrayDeque is a resizable-circular array implementation of the Deque interface. It is a good replacement for legacy Stack or LinkedList when you need a stack or queue.

## As a Stack (LIFO)
Use push/pop/peek (or addFirst/removeFirst/peekFirst) to treat ArrayDeque as a stack.

Example:
```java
import java.util.ArrayDeque;

ArrayDeque<Integer> stack = new ArrayDeque<>();
stack.push(10);         // push 10 (top)
stack.push(20);         // push 20 (new top)
int top = stack.pop();  // -> 20
int peek = stack.peek(); // -> 10
```

Alternate (same effect):
```java
stack.addFirst(30);
int x = stack.removeFirst();
int y = stack.peekFirst();
```

Iterating: the iterator of ArrayDeque traverses from front (top when used as stack) to back.

## As a Queue (FIFO)
Use add/offer/remove/poll/peek (or addLast/removeFirst/peekFirst) for queue behavior.

Example:
```java
ArrayDeque<Integer> queue = new ArrayDeque<>();
queue.add(1);            // enqueue 1 (head -> 1)
queue.add(2);            // enqueue 2
int head = queue.remove(); // -> 1
int front = queue.peek();  // -> next element (2)
```

Alternate (explicit deque methods):
```java
queue.addLast(3);
int q = queue.removeFirst(); // FIFO remove
int f = queue.peekFirst();
```

## Notes
- Complexity: most operations (push/pop/add/remove/peek) run in amortized O(1).
- Nulls: ArrayDeque does not permit null elements.
- Thread-safety: ArrayDeque is not synchronized. Use external synchronization or concurrent queues (e.g., ConcurrentLinkedQueue) for multi-threaded access.
- Capacity: grows as needed; no fixed capacity unless you wrap or restrict it.

