Here's a quick overview of the `LinkedHashSet` class in Java, which is a part of the `java.util` package. It is an implementation of the `Set` interface that uses a hash table with a linked list running through it, providing predictable iteration order (insertion order).

### Methods of `LinkedHashSet` with Example Code

1. **add(Object o):** Adds the specified element to the set if it is not already present.
2. **remove(Object o):** Removes the specified element from the set if it is present.
3. **contains(Object o):** Returns `true` if this set contains the specified element.
4. **size():** Returns the number of elements in the set.
5. **clear():** Removes all of the elements from the set.
6. **isEmpty():** Returns `true` if this set contains no elements.
7. **iterator():** Returns an iterator over the elements in this set in insertion order.

### Example Code for Each Method

Here is a Java code snippet demonstrating how to use these methods:

```java
import java.util.LinkedHashSet;
import java.util.Iterator;

public class LinkedHashSetExample {
    public static void main(String[] args) {
        // Create a LinkedHashSet
        LinkedHashSet<String> linkedHashSet = new LinkedHashSet<>();

        // 1. add(Object o)
        linkedHashSet.add("Apple");
        linkedHashSet.add("Banana");
        linkedHashSet.add("Orange");
        System.out.println("LinkedHashSet after adding elements: " + linkedHashSet);

        // 2. remove(Object o)
        linkedHashSet.remove("Banana");
        System.out.println("LinkedHashSet after removing 'Banana': " + linkedHashSet);

        // 3. contains(Object o)
        boolean containsApple = linkedHashSet.contains("Apple");
        System.out.println("Contains 'Apple'? " + containsApple);

        // 4. size()
        int size = linkedHashSet.size();
        System.out.println("Size of LinkedHashSet: " + size);

        // 5. clear()
        linkedHashSet.clear();
        System.out.println("LinkedHashSet after clear(): " + linkedHashSet);

        // 6. isEmpty()
        boolean isEmpty = linkedHashSet.isEmpty();
        System.out.println("Is LinkedHashSet empty? " + isEmpty);

        // Adding elements again for iteration example
        linkedHashSet.add("Mango");
        linkedHashSet.add("Grapes");
        linkedHashSet.add("Pineapple");

        // 7. iterator()
        System.out.print("Iterating over LinkedHashSet: ");
        Iterator<String> iterator = linkedHashSet.iterator();
        while (iterator.hasNext()) {
            System.out.print(iterator.next() + " ");
        }
    }
}
```

### Explanation of the Code

- **add()**: Adds elements "Apple", "Banana", and "Orange" to the `LinkedHashSet`.
- **remove()**: Removes "Banana" from the `LinkedHashSet`.
- **contains()**: Checks if "Apple" is present in the `LinkedHashSet`.
- **size()**: Returns the number of elements in the `LinkedHashSet`.
- **clear()**: Removes all elements from the `LinkedHashSet`.
- **isEmpty()**: Checks if the `LinkedHashSet` is empty after clearing.
- **iterator()**: Uses an iterator to iterate over the elements in insertion order.

This code demonstrates the use of all the basic methods provided by `LinkedHashSet` and how to iterate through its elements.
