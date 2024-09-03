# Collection in Java

Here's a list of important methods available in the `Collection` interface in Java, along with a one-line explanation and an example code snippet for each:

### Methods in the `Collection` Interface

1. **`add(E e)`**

   - **Explanation**: Adds the specified element to the collection.
   - **Example**:
     ```java
     Collection<String> collection = new ArrayList<>();
     collection.add("Apple");
     ```

2. **`addAll(Collection<? extends E> c)`**

   - **Explanation**: Adds all elements from the specified collection to this collection.
   - **Example**:
     ```java
     Collection<String> collection = new ArrayList<>();
     Collection<String> newItems = Arrays.asList("Banana", "Orange");
     collection.addAll(newItems);
     ```

3. **`clear()`**

   - **Explanation**: Removes all elements from the collection.
   - **Example**:
     ```java
     collection.clear();
     ```

4. **`contains(Object o)`**

   - **Explanation**: Returns `true` if the collection contains the specified element.
   - **Example**:
     ```java
     boolean hasApple = collection.contains("Apple");
     ```

5. **`containsAll(Collection<?> c)`**

   - **Explanation**: Returns `true` if the collection contains all elements in the specified collection.
   - **Example**:
     ```java
     boolean hasAll = collection.containsAll(Arrays.asList("Apple", "Banana"));
     ```

6. **`equals(Object o)`**

   - **Explanation**: Compares the specified object with the collection for equality.
   - **Example**:
     ```java
     boolean isEqual = collection.equals(new ArrayList<>(Arrays.asList("Apple", "Banana")));
     ```

7. **`hashCode()`**

   - **Explanation**: Returns the hash code value for the collection.
   - **Example**:
     ```java
     int hashCode = collection.hashCode();
     ```

8. **`isEmpty()`**

   - **Explanation**: Returns `true` if the collection contains no elements.
   - **Example**:
     ```java
     boolean empty = collection.isEmpty();
     ```

9. **`iterator()`**

   - **Explanation**: Returns an iterator over the elements in the collection.
   - **Example**:
     ```java
     Iterator<String> iterator = collection.iterator();
     while (iterator.hasNext()) {
         System.out.println(iterator.next());
     }
     ```

10. **`remove(Object o)`**

    - **Explanation**: Removes a single instance of the specified element from the collection, if it is present.
    - **Example**:
      ```java
      collection.remove("Apple");
      ```

11. **`removeAll(Collection<?> c)`**

    - **Explanation**: Removes all elements in the collection that are also contained in the specified collection.
    - **Example**:
      ```java
      collection.removeAll(Arrays.asList("Banana", "Orange"));
      ```

12. **`retainAll(Collection<?> c)`**

    - **Explanation**: Retains only the elements in the collection that are contained in the specified collection.
    - **Example**:
      ```java
      collection.retainAll(Arrays.asList("Apple", "Banana"));
      ```

13. **`size()`**

    - **Explanation**: Returns the number of elements in the collection.
    - **Example**:
      ```java
      int size = collection.size();
      ```

14. **`toArray()`**

    - **Explanation**: Returns an array containing all elements in the collection.
    - **Example**:
      ```java
      Object[] array = collection.toArray();
      ```

15. **`toArray(T[] a)`**
    - **Explanation**: Returns an array containing all elements in the collection; the runtime type of the returned array is that of the specified array.
    - **Example**:
      ```java
      String[] array = collection.toArray(new String[0]);
      ```

### Example of Using Multiple Methods Together

```java
import java.util.*;

public class CollectionExample {
    public static void main(String[] args) {
        Collection<String> collection = new ArrayList<>();

        // Adding elements
        collection.add("Apple");
        collection.addAll(Arrays.asList("Banana", "Orange"));

        // Checking size and contents
        System.out.println("Size: " + collection.size());  // Output: Size: 3
        System.out.println("Contains Apple: " + collection.contains("Apple"));  // Output: Contains Apple: true

        // Iterating over elements
        for (String fruit : collection) {
            System.out.println(fruit);
        }

        // Removing an element
        collection.remove("Banana");

        // Converting to array
        String[] array = collection.toArray(new String[0]);
        System.out.println("Array: " + Arrays.toString(array));  // Output: Array: [Apple, Orange]

        // Clearing the collection
        collection.clear();
        System.out.println("Is empty: " + collection.isEmpty());  // Output: Is empty: true
    }
}
```

This code demonstrates the use of various methods from the `Collection` interface, including adding, removing, checking size and contents, iterating, and converting to an array.
