An `ArrayQueue` is a queue implementation using a fixed-size array. It operates on a FIFO (First In, First Out) basis, meaning that elements are added to the end of the queue and removed from the front.

Here are the basic methods for an `ArrayQueue` in Java:

1. **Constructor**: Initializes the queue.
2. **enqueue(T element)**: Adds an element to the end of the queue.
3. **dequeue()**: Removes and returns the element at the front of the queue.
4. **peek()**: Returns the front element without removing it.
5. **isEmpty()**: Checks if the queue is empty.
6. **size()**: Returns the number of elements in the queue.
7. **iterator()**: Returns an iterator over the elements in the queue.

### Example Code: `ArrayQueue`

```java
import java.util.Iterator;
import java.util.NoSuchElementException;

public class ArrayQueue<T> implements Iterable<T> {
    private T[] queue;      // Array to store queue elements
    private int front;      // Index of the front element
    private int rear;       // Index of the next available position
    private int count;      // Number of elements in the queue
    private int capacity;   // Maximum size of the queue

    // Constructor to initialize the queue with a given capacity
    public ArrayQueue(int capacity) {
        this.capacity = capacity;
        this.queue = (T[]) new Object[capacity];
        this.front = 0;
        this.rear = 0;
        this.count = 0;
    }

    // Adds an element to the rear of the queue
    public void enqueue(T element) {
        if (count == capacity) {
            throw new IllegalStateException("Queue is full");
        }
        queue[rear] = element;
        rear = (rear + 1) % capacity; // Circular increment
        count++;
    }

    // Removes and returns the element from the front of the queue
    public T dequeue() {
        if (isEmpty()) {
            throw new NoSuchElementException("Queue is empty");
        }
        T element = queue[front];
        queue[front] = null;  // For garbage collection
        front = (front + 1) % capacity; // Circular increment
        count--;
        return element;
    }

    // Returns the front element without removing it
    public T peek() {
        if (isEmpty()) {
            throw new NoSuchElementException("Queue is empty");
        }
        return queue[front];
    }

    // Checks if the queue is empty
    public boolean isEmpty() {
        return count == 0;
    }

    // Returns the number of elements in the queue
    public int size() {
        return count;
    }

    // Returns an iterator to iterate over the elements in the queue
    @Override
    public Iterator<T> iterator() {
        return new ArrayQueueIterator();
    }

    // Inner class to implement the iterator
    private class ArrayQueueIterator implements Iterator<T> {
        private int index = front;
        private int numElementsIterated = 0;

        @Override
        public boolean hasNext() {
            return numElementsIterated < count;
        }

        @Override
        public T next() {
            if (!hasNext()) {
                throw new NoSuchElementException();
            }
            T element = queue[index];
            index = (index + 1) % capacity; // Circular increment
            numElementsIterated++;
            return element;
        }
    }

    // Example usage
    public static void main(String[] args) {
        ArrayQueue<Integer> queue = new ArrayQueue<>(5);

        // Enqueue elements
        queue.enqueue(1);
        queue.enqueue(2);
        queue.enqueue(3);
        System.out.println("Size after enqueue: " + queue.size());

        // Iterate through the queue
        for (int num : queue) {
            System.out.println("Iterated value: " + num);
        }

        // Dequeue elements
        System.out.println("Dequeued: " + queue.dequeue());
        System.out.println("Peek front element: " + queue.peek());
        System.out.println("Size after dequeue: " + queue.size());

        // Iterate again
        for (int num : queue) {
            System.out.println("Iterated value after dequeue: " + num);
        }
    }
}
```

### Explanation of Methods

1. **enqueue(T element)**: Adds an element to the end of the queue. If the queue is full, it throws an `IllegalStateException`.
2. **dequeue()**: Removes the element at the front of the queue and returns it. If the queue is empty, it throws a `NoSuchElementException`.
3. **peek()**: Returns the front element without removing it. If the queue is empty, it throws a `NoSuchElementException`.
4. **isEmpty()**: Returns `true` if the queue is empty; otherwise, `false`.
5. **size()**: Returns the current size of the queue.
6. **iterator()**: Returns an iterator that can be used to iterate over the elements in the queue.

### Example Output

```
Size after enqueue: 3
Iterated value: 1
Iterated value: 2
Iterated value: 3
Dequeued: 1
Peek front element: 2
Size after dequeue: 2
Iterated value after dequeue: 2
Iterated value after dequeue: 3
```

This example demonstrates the queue's basic operations and how to iterate through its elements.
