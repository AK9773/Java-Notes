# Vector in Java

Here's a list of `Vector` methods and properties in Java, along with one-line explanations and example code for each method:

### 1. **`add(E e)`**

- **Explanation:** Appends the specified element to the end of this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(10);  // Adds 10 to the vector
  ```

### 2. **`add(int index, E element)`**

- **Explanation:** Inserts the specified element at the specified position in this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(0, 20);  // Inserts 20 at index 0
  ```

### 3. **`addAll(Collection<? extends E> c)`**

- **Explanation:** Appends all elements in the specified collection to the end of this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  List<Integer> list = Arrays.asList(30, 40);
  vector.addAll(list);  // Adds 30 and 40 to the vector
  ```

### 4. **`addAll(int index, Collection<? extends E> c)`**

- **Explanation:** Inserts all elements in the specified collection into this vector at the specified position.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  List<Integer> list = Arrays.asList(50, 60);
  vector.addAll(0, list);  // Inserts 50 and 60 at index 0
  ```

### 5. **`clear()`**

- **Explanation:** Removes all elements from this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(70);
  vector.clear();  // Removes all elements
  ```

### 6. **`contains(Object o)`**

- **Explanation:** Returns `true` if this vector contains the specified element.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(80);
  boolean contains = vector.contains(80);  // Returns true
  ```

### 7. **`elementAt(int index)`**

- **Explanation:** Returns the element at the specified position in this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(90);
  int element = vector.elementAt(0);  // Returns 90
  ```

### 8. **`firstElement()`**

- **Explanation:** Returns the first element of this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(100);
  int first = vector.firstElement();  // Returns 100
  ```

### 9. **`lastElement()`**

- **Explanation:** Returns the last element of this vector.
- **Example:**
  ```java
  Vector<Integer> vector = new Vector<>();
  vector.add(110);
  int last = vector.lastElement();  // Returns 110
  ```

### 10. **`get(int index)`**

    - **Explanation:** Returns the element at the specified position in this vector.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(120);
      int element = vector.get(0);  // Returns 120
      ```

### 11. **`indexOf(Object o)`**

    - **Explanation:** Returns the index of the first occurrence of the specified element in this vector.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(130);
      int index = vector.indexOf(130);  // Returns 0
      ```

### 12. **`isEmpty()`**

    - **Explanation:** Returns `true` if this vector contains no elements.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      boolean empty = vector.isEmpty();  // Returns true
      ```

### 13. **`remove(Object o)`**

    - **Explanation:** Removes the first occurrence of the specified element from this vector.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(140);
      vector.remove((Integer) 140);  // Removes 140 from the vector
      ```

### 14. **`remove(int index)`**

    - **Explanation:** Removes the element at the specified position in this vector.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(150);
      vector.remove(0);  // Removes element at index 0
      ```

### 15. **`set(int index, E element)`**

    - **Explanation:** Replaces the element at the specified position in this vector with the specified element.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(160);
      vector.set(0, 170);  // Sets element at index 0 to 170
      ```

### 16. **`size()`**

    - **Explanation:** Returns the number of elements in this vector.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(180);
      int size = vector.size();  // Returns 1
      ```

### 17. **`toArray()`**

    - **Explanation:** Returns an array containing all elements in this vector.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.add(190);
      Object[] array = vector.toArray();  // Converts vector to array
      ```

### 18. **`ensureCapacity(int minCapacity)`**

    - **Explanation:** Increases the capacity of this vector, if necessary, to ensure that it can hold at least the number of elements specified by the minimum capacity argument.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>();
      vector.ensureCapacity(50);  // Ensures capacity of at least 50 elements
      ```

### 19. **`trimToSize()`**

    - **Explanation:** Trims the capacity of this vector to be the vector's current size.
    - **Example:**
      ```java
      Vector<Integer> vector = new Vector<>(100);
      vector.trimToSize();  // Trims capacity to current size
      ```

These are some of the commonly used methods and properties of the `Vector` class in Java. Each method is designed to manipulate the elements in a vector, providing various functionalities similar to those in `ArrayList` but with synchronization for thread safety.
