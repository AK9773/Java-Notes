The `TreeSet` class in Java is part of the `java.util` package and implements the `Set` interface, backed by a `TreeMap`. The elements in a `TreeSet` are stored in a sorted and ascending order. This class does not allow `null` elements and is not synchronized.

### Common Methods of `TreeSet`:

1. **`add(E e)`**: Adds the specified element to the set if it is not already present.
2. **`remove(Object o)`**: Removes the specified element from the set if it is present.
3. **`contains(Object o)`**: Returns `true` if this set contains the specified element.
4. **`size()`**: Returns the number of elements in the set.
5. **`isEmpty()`**: Returns `true` if this set contains no elements.
6. **`first()`**: Returns the first (lowest) element currently in this set.
7. **`last()`**: Returns the last (highest) element currently in this set.
8. **`pollFirst()`**: Retrieves and removes the first (lowest) element, or returns `null` if this set is empty.
9. **`pollLast()`**: Retrieves and removes the last (highest) element, or returns `null` if this set is empty.
10. **`iterator()`**: Returns an iterator over the elements in this set in ascending order.
11. **`descendingIterator()`**: Returns an iterator over the elements in this set in descending order.

### Example Code for Each Method:

Here's a Java example demonstrating how to use each of these methods:

```java
import java.util.Iterator;
import java.util.TreeSet;

public class TreeSetExample {
    public static void main(String[] args) {
        // Create a new TreeSet
        TreeSet<Integer> treeSet = new TreeSet<>();

        // Add elements to the TreeSet
        treeSet.add(10);
        treeSet.add(5);
        treeSet.add(20);
        treeSet.add(15);
        System.out.println("TreeSet after adding elements: " + treeSet);

        // Remove an element from the TreeSet
        treeSet.remove(15);
        System.out.println("TreeSet after removing 15: " + treeSet);

        // Check if an element is present in the TreeSet
        boolean containsFive = treeSet.contains(5);
        System.out.println("TreeSet contains 5: " + containsFive);

        // Get the size of the TreeSet
        int size = treeSet.size();
        System.out.println("Size of TreeSet: " + size);

        // Check if the TreeSet is empty
        boolean isEmpty = treeSet.isEmpty();
        System.out.println("TreeSet is empty: " + isEmpty);

        // Get the first (lowest) element in the TreeSet
        int firstElement = treeSet.first();
        System.out.println("First (lowest) element: " + firstElement);

        // Get the last (highest) element in the TreeSet
        int lastElement = treeSet.last();
        System.out.println("Last (highest) element: " + lastElement);

        // Retrieve and remove the first element
        int polledFirst = treeSet.pollFirst();
        System.out.println("Polled first element: " + polledFirst);
        System.out.println("TreeSet after polling first element: " + treeSet);

        // Retrieve and remove the last element
        int polledLast = treeSet.pollLast();
        System.out.println("Polled last element: " + polledLast);
        System.out.println("TreeSet after polling last element: " + treeSet);

        // Iterate through the TreeSet using iterator()
        System.out.print("Iterating TreeSet in ascending order: ");
        Iterator<Integer> iterator = treeSet.iterator();
        while (iterator.hasNext()) {
            System.out.print(iterator.next() + " ");
        }
        System.out.println();

        // Iterate through the TreeSet in descending order
        System.out.print("Iterating TreeSet in descending order: ");
        Iterator<Integer> descendingIterator = treeSet.descendingIterator();
        while (descendingIterator.hasNext()) {
            System.out.print(descendingIterator.next() + " ");
        }
    }
}
```

### Explanation:

- **Add Elements**: Adds elements in ascending order (sorted order) automatically.
- **Remove Element**: Removes a specified element.
- **Check Containment**: Checks whether a specific element is present in the set.
- **Size**: Returns the number of elements in the set.
- **Check Empty**: Checks if the set is empty or not.
- **First and Last Elements**: Retrieves the smallest or largest element respectively.
- **Poll First and Last Elements**: Retrieves and removes the smallest or largest element respectively.
- **Iterate**: Demonstrates iterating over elements in both ascending and descending orders.

This code demonstrates all the important methods of `TreeSet` along with how to iterate over the elements.
