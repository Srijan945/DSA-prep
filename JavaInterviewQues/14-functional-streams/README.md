# Functional Programming & Streams — Q&A

208. What is functional programming?
- Style emphasizing immutable data and functions as first-class citizens.

209. Can you give an example of functional programming?
- Using map/filter/reduce to transform collections instead of loops.

210. What is a stream?
- Sequence of elements supporting aggregate operations, lazily evaluated.

211. Explain about streams with an example?
- list.stream().filter(x->x>0).map(x->x*2).collect(Collectors.toList())

- what are intermediate operations in streams?
- Operations like filter, map, distinct — they return a new stream and are lazy.

212. What are terminal operations in streams?
- Operations like collect, forEach, reduce that trigger evaluation.

213. What are method references?
- Shorthand for lambda calling a method: Class::method or instance::method.

214. What are lambda expressions?
- Short anonymous function syntax (params -> body).

215. Can you give an example of lambda expression?
- (x, y) -> x + y

216. Can you explain the relationship between lambda expression and functional interfaces?
- Lambdas implement a functional interface (single abstract method).

217. What is a predicate?
- Functional interface taking one argument and returning boolean (Predicate<T>).

218. What is the functional interface - function?
- Function<T,R> maps T to R.

219. What is a consumer?
- Consumer<T> accepts a T and returns void (performs side-effects).

220. Can you give examples of functional interfaces with multiple arguments?
- BiFunction<T,U,R>, BiConsumer<T,U>, BinaryOperator<T>.
