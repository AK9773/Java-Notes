Here's an example of how to use a `PriorityQueue` in Java, including the main methods and how to iterate over it.

### 1. PriorityQueue Methods

The `PriorityQueue` class in Java is part of the `java.util` package and implements the `Queue` interface. It is an unbounded priority queue based on a priority heap.

Here are some commonly used methods of `PriorityQueue`:

- **`add(E e)`**: Inserts the specified element into the priority queue.
- **`offer(E e)`**: Inserts the specified element into the priority queue. Returns `true` upon success, and `false` if the insertion fails.
- **`peek()`**: Retrieves, but does not remove, the head of the queue, or returns `null` if the queue is empty.
- **`poll()`**: Retrieves and removes the head of the queue, or returns `null` if the queue is empty.
- **`remove(Object o)`**: Removes a single instance of the specified element from the queue, if it is present.
- **`size()`**: Returns the number of elements in the queue.
- **`isEmpty()`**: Returns `true` if the queue contains no elements.
- **`clear()`**: Removes all elements from the queue.

### 2. Example Code

Here's an example that demonstrates each of these methods and how to iterate over a `PriorityQueue`:

```java
import java.util.PriorityQueue;
import java.util.Iterator;

public class PriorityQueueExample {
    public static void main(String[] args) {
        // Creating a PriorityQueue
        PriorityQueue<Integer> pq = new PriorityQueue<>();

        // Adding elements to the PriorityQueue
        pq.add(30);
        pq.offer(20);
        pq.add(50);
        pq.offer(10);
        pq.add(40);

        // Displaying the size of the PriorityQueue
        System.out.println("Size of PriorityQueue: " + pq.size());

        // Peeking at the top element (smallest) of the PriorityQueue
        System.out.println("Head of PriorityQueue using peek(): " + pq.peek());

        // Iterating through the PriorityQueue using an iterator
        System.out.println("PriorityQueue elements:");
        Iterator<Integer> iterator = pq.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        // Polling (removing) elements from the PriorityQueue
        System.out.println("Removing the head of PriorityQueue using poll(): " + pq.poll());

        // Removing a specific element
        pq.remove(30);
        System.out.println("PriorityQueue after removing element 30: " + pq);

        // Checking if the PriorityQueue is empty
        System.out.println("Is PriorityQueue empty? " + pq.isEmpty());

        // Clearing all elements from the PriorityQueue
        pq.clear();
        System.out.println("PriorityQueue after clearing: " + pq);

        // Checking the size of the PriorityQueue after clearing
        System.out.println("Size of PriorityQueue after clearing: " + pq.size());
    }
}
```

### 3. Explanation of the Example

1. **Adding Elements**: The `add` and `offer` methods insert elements into the priority queue. The difference between them is that `add` throws an exception if the element cannot be added, while `offer` returns `false` in that case.
2. **Peeking**: The `peek` method retrieves, but does not remove, the head of the queue (the smallest element).
3. **Iterating**: An iterator is used to traverse the elements of the queue.
4. **Polling**: The `poll` method retrieves and removes the head of the queue. If the queue is empty, it returns `null`.
5. **Removing Elements**: The `remove` method removes a specific element if it exists.
6. **Checking for Empty**: The `isEmpty` method checks whether the queue is empty.
7. **Clearing the Queue**: The `clear` method removes all elements from the queue.

### Output of the Example

The output of the above code will look like this:

```
Size of PriorityQueue: 5
Head of PriorityQueue using peek(): 10
PriorityQueue elements:
10
20
50
30
40
Removing the head of PriorityQueue using poll(): 10
PriorityQueue after removing element 30: [20, 40, 50]
Is PriorityQueue empty? false
PriorityQueue after clearing: []
Size of PriorityQueue after clearing: 0
```

This example demonstrates the basic usage of `PriorityQueue` in Java and how to iterate over its elements.
