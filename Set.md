# Set in Java

In Java, the `Set` interface is part of the Java Collections Framework and represents a collection that cannot contain duplicate elements. The `Set` interface is implemented by various classes like `HashSet`, `LinkedHashSet`, and `TreeSet`.

### Common Methods in `Set`

1. **`add(E e)`**  
   Adds the specified element to the set if it is not already present.  
   **Example:**

   ```java
   Set<String> set = new HashSet<>();
   set.add("Apple");  // Adds "Apple" to the set
   ```

2. **`addAll(Collection<? extends E> c)`**  
   Adds all the elements from the specified collection to the set if they're not already present.  
   **Example:**

   ```java
   Set<String> set = new HashSet<>();
   set.addAll(Arrays.asList("Apple", "Banana"));  // Adds "Apple" and "Banana" to the set
   ```

3. **`clear()`**  
   Removes all elements from the set, making it empty.  
   **Example:**

   ```java
   set.clear();  // Clears all elements from the set
   ```

4. **`contains(Object o)`**  
   Returns `true` if the set contains the specified element.  
   **Example:**

   ```java
   boolean hasApple = set.contains("Apple");  // Checks if "Apple" is in the set
   ```

5. **`containsAll(Collection<?> c)`**  
   Returns `true` if the set contains all the elements in the specified collection.  
   **Example:**

   ```java
   boolean hasAll = set.containsAll(Arrays.asList("Apple", "Banana"));  // Checks if both "Apple" and "Banana" are in the set
   ```

6. **`isEmpty()`**  
   Returns `true` if the set contains no elements.  
   **Example:**

   ```java
   boolean empty = set.isEmpty();  // Checks if the set is empty
   ```

7. **`iterator()`**  
   Returns an iterator over the elements in the set.  
   **Example:**

   ```java
   Iterator<String> it = set.iterator();
   while (it.hasNext()) {
       System.out.println(it.next());  // Iterates through the set elements
   }
   ```

8. **`remove(Object o)`**  
   Removes the specified element from the set if it is present.  
   **Example:**

   ```java
   set.remove("Apple");  // Removes "Apple" from the set
   ```

9. **`removeAll(Collection<?> c)`**  
   Removes from the set all its elements that are contained in the specified collection.  
   **Example:**

   ```java
   set.removeAll(Arrays.asList("Apple", "Banana"));  // Removes "Apple" and "Banana" from the set
   ```

10. **`retainAll(Collection<?> c)`**  
    Retains only the elements in the set that are contained in the specified collection.  
    **Example:**

    ```java
    set.retainAll(Arrays.asList("Apple", "Banana"));  // Retains only "Apple" and "Banana" in the set
    ```

11. **`size()`**  
    Returns the number of elements in the set.  
    **Example:**

    ```java
    int size = set.size();  // Gets the size of the set
    ```

12. **`toArray()`**  
    Returns an array containing all the elements in the set.  
    **Example:**

    ```java
    Object[] array = set.toArray();  // Converts the set to an array
    ```

13. **`toArray(T[] a)`**  
    Returns an array containing all the elements in the set; the runtime type of the returned array is that of the specified array.  
    **Example:**
    ```java
    String[] array = set.toArray(new String[0]);  // Converts the set to a String array
    ```

### Example Usage

```java
import java.util.*;

public class SetExample {
    public static void main(String[] args) {
        Set<String> set = new HashSet<>();

        // add method
        set.add("Apple");
        set.add("Banana");

        // contains method
        System.out.println("Contains Apple? " + set.contains("Apple"));

        // size method
        System.out.println("Size: " + set.size());

        // iterator method
        Iterator<String> it = set.iterator();
        while (it.hasNext()) {
            System.out.println(it.next());
        }

        // remove method
        set.remove("Banana");

        // isEmpty method
        System.out.println("Is empty? " + set.isEmpty());

        // clear method
        set.clear();
    }
}
```

This example demonstrates how to use various methods of the `Set` interface to manipulate and interact with a set of elements.
