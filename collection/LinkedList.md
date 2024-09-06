# LinkedList in Java

Here's a list of commonly used `LinkedList` methods and properties in Java, along with a one-line explanation and example code for each:

### 1. **`add(E e)`**

- **Explanation:** Adds the specified element to the end of the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  ```

### 2. **`add(int index, E element)`**

- **Explanation:** Inserts the specified element at the specified position in the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.add(1, "B"); // ["A", "B"]
  ```

### 3. **`addFirst(E e)`**

- **Explanation:** Inserts the specified element at the beginning of the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("B"); // ["B"]
  list.addFirst("A"); // ["A", "B"]
  ```

### 4. **`addLast(E e)`**

- **Explanation:** Appends the specified element to the end of the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.addLast("B"); // ["A", "B"]
  ```

### 5. **`remove(int index)`**

- **Explanation:** Removes the element at the specified position in the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.add("B"); // ["A", "B"]
  list.remove(0); // ["B"]
  ```

### 6. **`remove(Object o)`**

- **Explanation:** Removes the first occurrence of the specified element from the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.add("B"); // ["A", "B"]
  list.remove("A"); // ["B"]
  ```

### 7. **`removeFirst()`**

- **Explanation:** Removes and returns the first element of the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.add("B"); // ["A", "B"]
  list.removeFirst(); // ["B"]
  ```

### 8. **`removeLast()`**

- **Explanation:** Removes and returns the last element of the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.add("B"); // ["A", "B"]
  list.removeLast(); // ["A"]
  ```

### 9. **`get(int index)`**

- **Explanation:** Returns the element at the specified position in the list.
- **Example:**
  ```java
  LinkedList<String> list = new LinkedList<>();
  list.add("A"); // ["A"]
  list.add("B"); // ["A", "B"]
  String element = list.get(1); // "B"
  ```

### 10. **`getFirst()`**

    - **Explanation:** Returns the first element in the list.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      list.add("B"); // ["A", "B"]
      String element = list.getFirst(); // "A"
      ```

### 11. **`getLast()`**

    - **Explanation:** Returns the last element in the list.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      list.add("B"); // ["A", "B"]
      String element = list.getLast(); // "B"
      ```

### 12. **`contains(Object o)`**

    - **Explanation:** Checks if the list contains the specified element.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      boolean containsB = list.contains("B"); // false
      ```

### 13. **`size()`**

    - **Explanation:** Returns the number of elements in the list.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      int size = list.size(); // 1
      ```

### 14. **`clear()`**

    - **Explanation:** Removes all elements from the list.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      list.add("B"); // ["A", "B"]
      list.clear(); // []
      ```

### 15. **`isEmpty()`**

    - **Explanation:** Checks if the list is empty.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      boolean isEmpty = list.isEmpty(); // true
      ```

### 16. **`iterator()`**

    - **Explanation:** Returns an iterator over the elements in the list.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      Iterator<String> it = list.iterator();
      while (it.hasNext()) {
          System.out.println(it.next());
      }
      ```

### 17. **`offer(E e)`**

    - **Explanation:** Inserts the specified element at the end of the list.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.offer("A"); // ["A"]
      ```

### 18. **`poll()`**

    - **Explanation:** Retrieves and removes the head (first element) of the list, or returns `null` if the list is empty.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      String element = list.poll(); // "A"
      ```

### 19. **`peek()`**

    - **Explanation:** Retrieves, but does not remove, the head (first element) of the list, or returns `null` if the list is empty.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      String element = list.peek(); // "A"
      ```

### 20. **`descendingIterator()`**

    - **Explanation:** Returns an iterator over the elements in the list in reverse sequential order.
    - **Example:**
      ```java
      LinkedList<String> list = new LinkedList<>();
      list.add("A"); // ["A"]
      list.add("B"); // ["A", "B"]
      Iterator<String> it = list.descendingIterator();
      while (it.hasNext()) {
          System.out.println(it.next()); // B A
      }
      ```

These methods provide a comprehensive overview of the operations you can perform on a `LinkedList` in Java.
