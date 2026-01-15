# Collections — Q&A

134. Why do we need collections in Java?
- To store, retrieve and manipulate groups of objects with common APIs.

135. What are the important interfaces in the collection hierarchy?
- Collection, List, Set, Queue, Deque, Map (Map is separate but related).

136. What are the important methods that are declared in the collection interface?
- add, remove, contains, iterator, size, isEmpty, clear, toArray.

137. Can you explain briefly about the List interface?
- Ordered collection allowing duplicates and positional access.

138. Explain about ArrayList with an example?
- Resizable array implementation of List; allows fast random access, slower inserts/removals in middle.

139. Can an ArrayList have duplicate elements?
- Yes.

140. How do you iterate around an ArrayList using iterator?
- Iterator<E> it = list.iterator(); while(it.hasNext()) { E e = it.next(); }

141. How do you sort an ArrayList?
- Collections.sort(list) for natural order or Collections.sort(list, comparator).

142. How do you sort elements in an ArrayList using comparable interface?
- Elements implement Comparable and provide compareTo; use Collections.sort(list).

143. How do you sort elements in an ArrayList using comparator interface?
- Provide a Comparator and call Collections.sort(list, comparator).

144. What is vector class? How is it different from an ArrayList?
- Legacy synchronized list implementation; ArrayList is unsynchronized and preferred.

145. What is linkedList? What interfaces does it implement? How is it different from an ArrayList?
- Doubly-linked list implementing List and Deque; faster insertions/removals, slower random access.

146. Can you briefly explain about the Set interface?
- Collection with no duplicate elements; unordered.

147. What are the important interfaces related to the Set interface?
- SortedSet, NavigableSet.

148. What is the difference between Set and sortedSet interfaces?
- SortedSet maintains elements in sorted order.

149. Can you give examples of classes that implement the Set interface?
- HashSet, LinkedHashSet, TreeSet.

150. What is a HashSet?
- Backed by a HashMap; no order guarantee, allows null.

151. What is a linkedHashSet? How is different from a HashSet?
- Maintains insertion order using a linked list in addition to hashing.

152. What is a TreeSet? How is different from a HashSet?
- Sorted set backed by a Red-Black tree; elements ordered, no nulls allowed (depending on comparator).

153. Can you give examples of implementations of navigableSet?
- TreeSet implements NavigableSet.

154. Explain briefly about Queue interface?
- FIFO collection for holding elements prior to processing.

155. What are the important interfaces related to the Queue interface?
- Deque, BlockingQueue.

156. Explain about the Deque interface?
- Double-ended queue supporting insertion/removal at both ends (ArrayDeque, LinkedList).

157. Explain the BlockingQueue interface?
- Queue supporting operations that wait for space or elements (used in producer-consumer).

158. What is a priorityQueue?
- Unordered queue where elements are ordered by priority (heap-backed).

159. Can you give example implementations of the BlockingQueue interface?
- ArrayBlockingQueue, LinkedBlockingQueue, PriorityBlockingQueue, SynchronousQueue.

160. Can you briefly explain about the Map interface?
- Key-value mapping; no duplicate keys.

161. What is difference between Map and sortedMap?
- SortedMap maintains keys in natural/order order.

162. What is a HashMap?
- Hash table based Map implementation; allows null keys/values, unordered.

163. What are the different methods in a Hash Map?
- put, get, remove, containsKey, containsValue, keySet, entrySet, values, putIfAbsent, compute, merge.

164. What is a TreeMap? How is different from a HashMap?
- Sorted map backed by a tree; keys ordered, no null keys allowed typically.

165. Can you give an example of implementation of navigableMap interface?
- TreeMap implements NavigableMap.

166. What are the static methods present in the collections class?
- Collections utility methods: sort, binarySearch, reverse, unmodifiableList, synchronizedList, emptyList, etc.
