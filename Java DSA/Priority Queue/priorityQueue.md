### Commonly Used Functions of PriorityQueue in Java

1. **Add an Element**  
   `boolean add(E e)` - Inserts the specified element into the priority queue.

2. **Offer an Element**  
   `boolean offer(E e)` - Inserts the specified element into the priority queue. Similar to `add()` but returns `false` if the queue is full.

3. **Peek the Head**  
   `E peek()` - Retrieves, but does not remove, the head of the queue, or returns `null` if the queue is empty.

4. **Poll the Head**  
   `E poll()` - Retrieves and removes the head of the queue, or returns `null` if the queue is empty.

5. **Remove an Element**  
   `boolean remove(Object o)` - Removes a single instance of the specified element from the queue, if present.

6. **Check Size**  
   `int size()` - Returns the number of elements in the queue.

7. **Check if Empty**  
   `boolean isEmpty()` - Returns `true` if the queue contains no elements.

8. **Clear the Queue**  
   `void clear()` - Removes all elements from the queue.

9. **Iterate Through Elements**  
   `Iterator<E> iterator()` - Returns an iterator over the elements in the queue.

10. **Contains an Element**  
    `boolean contains(Object o)` - Returns `true` if the queue contains the specified element.

### Example Usage
```java
import java.util.PriorityQueue;

public class Main {
    public static void main(String[] args) {
        PriorityQueue<Integer> pq = new PriorityQueue<>();

        // Add elements
        pq.add(10);
        pq.offer(20);

        // Peek and poll
        System.out.println("Head: " + pq.peek());
        System.out.println("Removed Head: " + pq.poll());

        // Check size and if empty
        System.out.println("Size: " + pq.size());
        System.out.println("Is Empty: " + pq.isEmpty());

        // Clear the queue
        pq.clear();
    }
}
```
