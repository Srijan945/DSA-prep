# Miscellaneous Topics — Q&A

109. What are the default values in an array?
- Numeric: 0, boolean: false, object refs: null, char: '\u0000'.

110. How do you loop around an array using enhanced for loop?
- for (Type t : array) { ... }

111. How do you print the content of an array?
- Use Arrays.toString(array) or Arrays.deepToString for nested arrays.

112. How do you compare two arrays?
- Arrays.equals for one-dimensional; Arrays.deepEquals for nested.

113. What is an enum?
- A special type that defines a fixed set of constants.

114. Can you use a switch statement around an enum?
- Yes.

115. What are variable arguments or varargs?
- Method parameter that accepts variable number of arguments using ... syntax.

116. What are asserts used for?
- Internal sanity checks during development; throw AssertionError when condition false.

117. When should asserts be used?
- To check programmer assumptions, not for runtime input validation.

118. What is garbage collection?
- Automatic memory management that reclaims unused objects.

119. Can you explain garbage collection with an example?
- Unreferenced objects become eligible; GC reclaims their memory.

120. When is garbage collection run?
- JVM decides; can be triggered but not guaranteed at a specific time.

121. What are best practices on garbage collection?
- Avoid unnecessary object creation, null out long-lived references, prefer primitives/objects appropriately.

122. What are initialization blocks?
- Blocks that run during object construction: static initializer and instance initializer.

123. What is a static initializer?
- static { ... } runs once when class is loaded.

124. What is an instance initializer block?
- { ... } runs before constructor for each instance.

125. What is tokenizing?
- Splitting string into tokens using delimiters.

126. Can you give an example of tokenizing?
- String.split(",") or StringTokenizer/Scanner usage.

127. What is serialization?
- Converting object state to a byte stream for persistence or transfer.

128. How do you serialize an object using serializable interface?
- Implement java.io.Serializable and write via ObjectOutputStream.

129. How do you de-serialize in Java?
- Read with ObjectInputStream and cast to target type.

130. What do you do if only parts of the object have to be serialized?
- Mark fields transient or implement custom writeObject/readObject.

131. How do you serialize a hierarchy of objects?
- Ensure all referenced objects are Serializable or mark transient.

132. Are the constructors in an object invoked when it is de-serialized?
- No for Serializable; yes for Externalizable or when superclass not Serializable.

133. Are the values of static variables stored when an object is serialized?
- No; static fields are not serialized.
