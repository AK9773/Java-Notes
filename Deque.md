The `Deque` (Double-Ended Queue) interface in Java extends the `Queue` interface and provides support for operations that can be performed at both ends of the deque. Here's a list of common methods provided by the `Deque` interface, along with example code to demonstrate how to use each method.

### 1. Deque Methods

- **addFirst(E e)**: Inserts the specified element at the front of this deque.
- **addLast(E e)**: Inserts the specified element at the end of this deque.
- **offerFirst(E e)**: Inserts the specified element at the front of this deque.
- **offerLast(E e)**: Inserts the specified element at the end of this deque.
- **removeFirst()**: Removes and returns the first element of this deque.
- **removeLast()**: Removes and returns the last element of this deque.
- **pollFirst()**: Retrieves and removes the first element of this deque, or returns `null` if this deque is empty.
- **pollLast()**: Retrieves and removes the last element of this deque, or returns `null` if this deque is empty.
- **getFirst()**: Retrieves, but does not remove, the first element of this deque.
- **getLast()**: Retrieves, but does not remove, the last element of this deque.
- **peekFirst()**: Retrieves, but does not remove, the first element of this deque, or returns `null` if this deque is empty.
- **peekLast()**: Retrieves, but does not remove, the last element of this deque, or returns `null` if this deque is empty.
- **removeFirstOccurrence(Object o)**: Removes the first occurrence of the specified element from this deque.
- **removeLastOccurrence(Object o)**: Removes the last occurrence of the specified element from this deque.

### 2. Example Code for Each Method

Here's a Java code snippet to demonstrate how to use these methods:

```java
import java.util.Deque;
import java.util.LinkedList;

public class DequeExample {
    public static void main(String[] args) {
        // Creating a Deque using LinkedList
        Deque<String> deque = new LinkedList<>();

        // Adding elements to the Deque
        deque.addFirst("Alice");
        deque.addLast("Bob");
        deque.offerFirst("Charlie");
        deque.offerLast("David");

        // Printing the Deque
        System.out.println("Deque after additions: " + deque);

        // Accessing elements from the Deque
        System.out.println("First Element: " + deque.getFirst()); // Charlie
        System.out.println("Last Element: " + deque.getLast()); // David
        System.out.println("Peek First Element: " + deque.peekFirst()); // Charlie
        System.out.println("Peek Last Element: " + deque.peekLast()); // David

        // Removing elements from the Deque
        deque.removeFirst(); // Removes Charlie
        deque.removeLast(); // Removes David
        System.out.println("Deque after removing first and last: " + deque);

        deque.pollFirst(); // Removes Alice
        deque.pollLast(); // Removes Bob
        System.out.println("Deque after polling first and last: " + deque);

        // Adding elements again for removal by occurrence
        deque.add("Alice");
        deque.add("Bob");
        deque.add("Alice");

        // Removing by occurrence
        deque.removeFirstOccurrence("Alice");
        System.out.println("Deque after removing first occurrence of 'Alice': " + deque);

        deque.removeLastOccurrence("Alice");
        System.out.println("Deque after removing last occurrence of 'Alice': " + deque);

        // Iterating over the Deque
        System.out.println("Iterating over Deque:");
        for (String name : deque) {
            System.out.println(name);
        }
    }
}
```

### Explanation

- **Adding Elements**: The `addFirst()` and `offerFirst()` methods add elements to the front, while `addLast()` and `offerLast()` add elements to the end.
- **Accessing Elements**: `getFirst()`, `getLast()`, `peekFirst()`, and `peekLast()` are used to access elements without removing them.
- **Removing Elements**: `removeFirst()` and `removeLast()` remove elements from both ends, while `pollFirst()` and `pollLast()` perform the same but return `null` if the deque is empty.
- **Removing by Occurrence**: `removeFirstOccurrence()` and `removeLastOccurrence()` remove elements based on their occurrence.
- **Iteration**: The for-each loop demonstrates iterating over the deque.

### Output

The output of the above code will look something like:

```
Deque after additions: [Charlie, Alice, Bob, David]
First Element: Charlie
Last Element: David
Peek First Element: Charlie
Peek Last Element: David
Deque after removing first and last: [Alice, Bob]
Deque after polling first and last: []
Deque after removing first occurrence of 'Alice': [Bob, Alice]
Deque after removing last occurrence of 'Alice': [Bob]
Iterating over Deque:
Bob
```

These examples cover most of the `Deque` interface methods and demonstrate their usage in a Java program.
