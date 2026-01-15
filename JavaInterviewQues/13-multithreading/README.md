# Multithreading — Q&A

185. What is the need for threads in Java?
- To perform concurrent tasks, improve responsiveness and resource utilization.

186. How do you create a thread?
- Extend Thread or implement Runnable/Callable, or use ExecutorService.

187. How do you create a thread by extending thread class?
- class MyThread extends Thread { public void run() { ... } }

188. How do you create a thread by implementing runnable interface?
- class MyTask implements Runnable { public void run() { ... } } new Thread(new MyTask()).start();

189. How do you run a thread in Java?
- Call start(), not run().

190. What are the different states of a thread?
- NEW, RUNNABLE, BLOCKED, WAITING, TIMED_WAITING, TERMINATED.

191. What is priority of a thread? How do you change the priority of a thread?
- Priority is scheduling hint (1–10); use setPriority(int).

192. What is executorservice?
- High-level API for managing a pool of threads and task execution.

193. Can you give an example for executorservice?
- ExecutorService ex = Executors.newFixedThreadPool(4); ex.submit(task);

194. Explain different ways of creating executor services . 
- newFixedThreadPool, newCachedThreadPool, newSingleThreadExecutor, newScheduledThreadPool.

195. How do you check whether an executionservice task executed successfully?
- Future.get() returns result or throws ExecutionException if failed.

196. What is callable? How do you execute a callable from executionservice?
- Callable returns a value and can throw checked exceptions; submit Callable to ExecutorService returns Future.

197. What is synchronization of threads?
- Mechanism to control access to shared resources to avoid race conditions.

198. Can you give an example of a synchronized block?
- synchronized(lock) { /* critical section */ }

199. Can a static method be synchronized?
- Yes; synchronized static method locks the Class object.

200. What is the use of join method in threads?
- Waits for another thread to finish before continuing.

201. Describe a few other important methods in threads?
- sleep, interrupt, isAlive, getState, setDaemon.

202. What is a deadlock?
- Situation where two or more threads wait indefinitely for locks held by each other.

203. What are the important methods in Java for inter-thread communication?
- wait, notify, notifyAll (must be called within synchronized block).

204. What is the use of wait method?
- Releases lock and waits until notified.

205. What is the use of notify method?
- Wakes one waiting thread.

206. What is the use of notifyall method?
- Wakes all waiting threads.

207. Can you write a synchronized program with wait and notify methods?
- Yes; typical producer-consumer pattern uses synchronized, wait, notify/notifyAll. Provide code snippet if needed.
