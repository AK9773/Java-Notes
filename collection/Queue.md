# Queue in Java

Here's a comprehensive list of `Queue` methods in Java, with one-line explanations and example code for each:

### 1. **`add(E e)`**

- **Explanation**: Inserts the specified element into the queue; throws an exception if the queue is full.
- **Example**:
  ```java
  Queue<Integer> queue = new LinkedList<>();
  queue.add(1);  // Adds 1 to the queue
  ```

### 2. **`offer(E e)`**

- **Explanation**: Inserts the specified element into the queue; returns `false` if the queue is full.
- **Example**:
  ```java
  Queue<Integer> queue = new LinkedList<>();
  queue.offer(2);  // Adds 2 to the queue
  ```

### 3. **`remove()`**

- **Explanation**: Retrieves and removes the head of the queue; throws an exception if the queue is empty.
- **Example**:
  ```java
  queue.remove();  // Removes and returns the head element (1)
  ```

### 4. **`poll()`**

- **Explanation**: Retrieves and removes the head of the queue; returns `null` if the queue is empty.
- **Example**:
  ```java
  queue.poll();  // Removes and returns the head element (2)
  ```

### 5. **`element()`**

- **Explanation**: Retrieves, but does not remove, the head of the queue; throws an exception if the queue is empty.
- **Example**:
  ```java
  queue.add(3);
  int head = queue.element();  // Returns the head element (3)
  ```

### 6. **`peek()`**

- **Explanation**: Retrieves, but does not remove, the head of the queue; returns `null` if the queue is empty.
- **Example**:
  ```java
  int head = queue.peek();  // Returns the head element (3) without removing it
  ```

### 7. **`size()`**

- **Explanation**: Returns the number of elements in the queue.
- **Example**:
  ```java
  int size = queue.size();  // Returns the size of the queue (1)
  ```

### 8. **`isEmpty()`**

- **Explanation**: Returns `true` if the queue contains no elements.
- **Example**:
  ```java
  boolean empty = queue.isEmpty();  // Returns false since the queue is not empty
  ```

### 9. **`contains(Object o)`**

- **Explanation**: Returns `true` if the queue contains the specified element.
- **Example**:
  ```java
  boolean containsThree = queue.contains(3);  // Returns true if the queue contains 3
  ```

### 10. **`clear()`**

- **Explanation**: Removes all elements from the queue.
- **Example**:
  ```java
  queue.clear();  // Empties the queue
  ```

### 11. **`iterator()`**

- **Explanation**: Returns an iterator over the elements in the queue.
- **Example**:
  ```java
  Iterator<Integer> iterator = queue.iterator();
  while (iterator.hasNext()) {
      System.out.println(iterator.next());  // Iterates over the queue elements
  }
  ```

### Example of Using Multiple Methods Together

Here’s an example that demonstrates the use of multiple `Queue` methods:

```java
import java.util.*;

public class QueueExample {
    public static void main(String[] args) {
        Queue<Integer> queue = new LinkedList<>();

        // Adding elements
        queue.add(1);
        queue.offer(2);

        // Accessing the head
        System.out.println("Head: " + queue.element());  // Outputs 1
        System.out.println("Head: " + queue.peek());     // Outputs 1

        // Removing elements
        queue.remove();  // Removes 1
        System.out.println("Polled: " + queue.poll());  // Removes and returns 2

        // Checking size and emptiness
        System.out.println("Is empty: " + queue.isEmpty());  // Outputs true

        // Adding more elements
        queue.add(3);
        queue.add(4);

        // Iterating over the queue
        for (int num : queue) {
            System.out.println(num);  // Outputs 3 and 4
        }

        // Clearing the queue
        queue.clear();
        System.out.println("Is empty after clear: " + queue.isEmpty());  // Outputs true
    }
}
```

This example covers how to add, access, remove, check, and iterate over elements in a `Queue`.
