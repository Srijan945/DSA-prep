# Java Collections Framework — Hierarchy & Detailed Info

This note summarizes the main interfaces and commonly used implementations in the Java Collections Framework, with short facts about purpose, ordering, duplicates, nulls, thread-safety and typical complexity.

## Root
- Iterable
  - Purpose: Single method iterator() — enables foreach.
  - Common methods: iterator(), forEach().
  - Implemented by most collection interfaces.

## Collection (root for most collections)
- Purpose: Base interface for groups of elements.
- Common methods: add(E), remove(Object), contains(Object), size(), iterator(), stream().

### List
- Purpose: Ordered collection with positional access.
- Allows duplicates: Yes.
- Order: Insertion/positional — elements accessible by index.
- Nulls: Allowed (implementation dependent).
- Thread-safety: Not synchronized by default.
- Common implementations: ArrayList, LinkedList, Vector (legacy), CopyOnWriteArrayList (concurrent).
- Typical complexity:
  - ArrayList: get O(1), add (amortized) O(1), add/remove at arbitrary index O(n).
  - LinkedList: add/remove at ends O(1), random access O(n).
- Typical methods: get(int), set(int, E), add(int, E), remove(int), indexOf(Object).

### Set
- Purpose: Collection that disallows duplicates.
- Allows duplicates: No.
- Nulls: Depends on implementation (HashSet allows one null; TreeSet depends on Comparator).
- Thread-safety: Not synchronized by default.
- Common implementations:
  - HashSet — no ordering, O(1) average ops.
  - LinkedHashSet — insertion-order iteration.
  - TreeSet — sorted order (implements NavigableSet), O(log n) ops.
- Typical methods: add(E), contains(Object), remove(Object).

### SortedSet / NavigableSet (subinterfaces of Set)
- SortedSet: Maintains elements in sorted order (natural order or Comparator).
- NavigableSet: Adds navigation methods (lower, floor, ceiling, higher, pollFirst/Last, descendingSet).
- Implementations: TreeSet.

### Queue
- Purpose: Hold elements prior to processing (FIFO common) and provide queue operations.
- Allows duplicates: Yes.
- Order: FIFO or priority-based depending on implementation.
- Nulls: Generally not permitted in many queues (PriorityQueue forbids null).
- Common implementations:
  - LinkedList (also implements Deque), ArrayDeque — double-ended and efficient at both ends.
  - PriorityQueue — ordered by priority (not FIFO).
- Typical methods: offer(E), poll(), peek(), remove(), element().

### Deque (double-ended queue)
- Purpose: Insert/remove at both ends.
- Use cases: stack (as LIFO) or queue (as FIFO).
- Common implementations: ArrayDeque, LinkedList.
- Typical methods: addFirst, addLast, removeFirst, removeLast, peekFirst, peekLast, push, pop.

## Map (not a Collection)
- Purpose: Key → Value mapping; keys are unique.
- Duplicate keys: No (key uniqueness); values can duplicate.
- Nulls:
  - HashMap/LinkedHashMap: allow null key and null values (one null key).
  - TreeMap: null key disallowed unless Comparator accepts null.
- Thread-safety: Not synchronized by default.
- Common implementations:
  - HashMap — no ordering, O(1) average lookup.
  - LinkedHashMap — predictable iteration order (insertion or access-order).
  - TreeMap — sorted by key, O(log n) ops (implements NavigableMap).
  - ConcurrentHashMap — concurrent access, no null keys/values.
  - WeakHashMap — keys held weakly for GC-based caches.
- Typical methods: put(K,V), get(Object), remove(Object), containsKey(Object), keySet(), values(), entrySet().

### SortedMap / NavigableMap (subinterfaces of Map)
- SortedMap: Maintains keys in sorted order.
- NavigableMap: Adds navigation methods (lowerEntry, floorEntry, ceilingEntry, higherEntry, pollFirstEntry, pollLastEntry, descendingMap).
- Implementation: TreeMap.

## Legacy & Concurrent Variants
- Legacy classes: Vector, Hashtable — synchronized older classes (use modern alternatives).
- Concurrent variants: ConcurrentHashMap, CopyOnWriteArrayList, ConcurrentLinkedQueue, etc. — provide thread-safety with different concurrency characteristics.

## Performance (general guidelines)
- Array-based vs linked:
  - ArrayList: random access O(1), insertion at end O(1) amortized, arbitrary insert/remove O(n).
  - LinkedList: insertion/removal at ends O(1), random access O(n).
- Hash-based vs tree-based:
  - HashSet/HashMap: O(1) average for add/get/remove; O(n) worst-case (hash collisions).
  - TreeSet/TreeMap: O(log n) for add/get/remove.
- Queue operations are typically O(1) for deque implementations; priority queues are O(log n) for insertion/removal.

## Common usage notes
- Choose List when you need positional access or allow duplicates.
- Choose Set for uniqueness and membership testing.
- Choose Map when mapping keys to values (lookup by key).
- Use LinkedHash* when deterministic iteration order matters.
- Use Tree* when sorted order or range queries are needed.
- Prefer concurrent implementations for multi-threaded access patterns instead of synchronizing standard collections manually.

This is a concise reference; consult the Javadoc for precise method contracts, concurrency semantics and fail-fast behavior.
