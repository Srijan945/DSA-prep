# Advanced Collections — Q&A

167. What is the difference between synchronized and concurrent collections in Java?
- Synchronized collections use coarse-grained locking; concurrent collections use fine-grained algorithms for better concurrency.

168. Explain about the new concurrent collections in Java?
- java.util.concurrent includes ConcurrentHashMap, ConcurrentLinkedQueue, CopyOnWriteArrayList, BlockingQueue implementations.

169. Explain about copyonwrite concurrent collections approach?
- On write, a fresh copy of underlying array is created; reads are lock-free and see a consistent snapshot.

170. What is compareandswap approach?
- Atomic operation that updates a value if it matches expected value; used in lock-free algorithms.

171. What is a lock? How is it different from using synchronized approach?
- Lock (java.util.concurrent.locks.Lock) offers more flexible locking (tryLock, timed lock) than synchronized (intrinsic lock).

172. What is initial capacity of a Java collection?
- The starting size of internal storage (e.g., initial capacity of ArrayList or HashMap).

173. What is load factor?
- Threshold that triggers rehash/resizing (HashMap default 0.75).

174. When does a Java collection throw UnsupportedOperationException?
- When an operation is not supported by the collection implementation (e.g., unmodifiable collections).

175. What is difference between fail-safe and fail-fast iterators?
- Fail-fast throw ConcurrentModificationException on structural modification; fail-safe operate on a copy and don't throw.

176. What are atomic operations in Java?
- Operations on atomic classes (AtomicInteger, AtomicReference) that are thread-safe without synchronization.

177. What is BlockingQueue in Java?
- Queue that waits when retrieving from empty or inserting into full queue; used in producer-consumer patterns.
