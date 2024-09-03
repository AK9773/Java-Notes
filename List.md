# List in Java

The `List` interface in Java is part of the Java Collections Framework and represents an ordered collection (also known as a sequence). Lists can contain duplicate elements and allow positional access to elements.

Here’s a comprehensive list of the methods provided by the `List` interface, along with a brief explanation and example code for each method:

### List Methods in Java

1. **`add(E e)`**  
   Adds an element to the end of the list.

   ```java
   List<String> list = new ArrayList<>();
   list.add("Apple");
   System.out.println(list);  // Output: [Apple]
   ```

2. **`add(int index, E element)`**  
   Inserts the specified element at the specified position in the list.

   ```java
   list.add(0, "Banana");
   System.out.println(list);  // Output: [Banana, Apple]
   ```

3. **`addAll(Collection<? extends E> c)`**  
   Appends all elements in the specified collection to the end of the list.

   ```java
   List<String> moreFruits = Arrays.asList("Orange", "Mango");
   list.addAll(moreFruits);
   System.out.println(list);  // Output: [Banana, Apple, Orange, Mango]
   ```

4. **`addAll(int index, Collection<? extends E> c)`**  
   Inserts all elements in the specified collection at the specified position in the list.

   ```java
   List<String> moreFruits = Arrays.asList("Grapes", "Pineapple");
   list.addAll(1, moreFruits);
   System.out.println(list);  // Output: [Banana, Grapes, Pineapple, Apple, Orange, Mango]
   ```

5. **`clear()`**  
   Removes all elements from the list.

   ```java
   list.clear();
   System.out.println(list);  // Output: []
   ```

6. **`contains(Object o)`**  
   Returns `true` if the list contains the specified element.

   ```java
   boolean hasApple = list.contains("Apple");
   System.out.println(hasApple);  // Output: false
   ```

7. **`containsAll(Collection<?> c)`**  
   Returns `true` if the list contains all elements in the specified collection.

   ```java
   boolean hasAll = list.containsAll(Arrays.asList("Apple", "Banana"));
   System.out.println(hasAll);  // Output: false
   ```

8. **`get(int index)`**  
   Returns the element at the specified position in the list.

   ```java
   list.addAll(Arrays.asList("Apple", "Banana", "Mango"));
   String fruit = list.get(1);
   System.out.println(fruit);  // Output: Banana
   ```

9. **`indexOf(Object o)`**  
   Returns the index of the first occurrence of the specified element, or `-1` if not found.

   ```java
   int index = list.indexOf("Mango");
   System.out.println(index);  // Output: 2
   ```

10. **`lastIndexOf(Object o)`**  
    Returns the index of the last occurrence of the specified element, or `-1` if not found.

    ```java
    list.add("Apple");
    int lastIndex = list.lastIndexOf("Apple");
    System.out.println(lastIndex);  // Output: 3
    ```

11. **`isEmpty()`**  
    Returns `true` if the list contains no elements.

    ```java
    boolean empty = list.isEmpty();
    System.out.println(empty);  // Output: false
    ```

12. **`remove(int index)`**  
    Removes the element at the specified position in the list.

    ```java
    list.remove(2);
    System.out.println(list);  // Output: [Apple, Banana, Apple]
    ```

13. **`remove(Object o)`**  
    Removes the first occurrence of the specified element from the list.

    ```java
    list.remove("Apple");
    System.out.println(list);  // Output: [Banana, Apple]
    ```

14. **`removeAll(Collection<?> c)`**  
    Removes all elements in the list that are contained in the specified collection.

    ```java
    list.removeAll(Arrays.asList("Apple", "Banana"));
    System.out.println(list);  // Output: []
    ```

15. **`retainAll(Collection<?> c)`**  
    Retains only the elements in the list that are contained in the specified collection.

    ```java
    list.addAll(Arrays.asList("Apple", "Banana", "Mango"));
    list.retainAll(Arrays.asList("Apple", "Mango"));
    System.out.println(list);  // Output: [Apple, Mango]
    ```

16. **`set(int index, E element)`**  
    Replaces the element at the specified position with the specified element.

    ```java
    list.set(1, "Orange");
    System.out.println(list);  // Output: [Apple, Orange]
    ```

17. **`size()`**  
    Returns the number of elements in the list.

    ```java
    int size = list.size();
    System.out.println(size);  // Output: 2
    ```

18. **`subList(int fromIndex, int toIndex)`**  
    Returns a view of the portion of the list between the specified `fromIndex`, inclusive, and `toIndex`, exclusive.

    ```java
    List<String> sublist = list.subList(0, 1);
    System.out.println(sublist);  // Output: [Apple]
    ```

19. **`toArray()`**  
    Returns an array containing all elements in the list.

    ```java
    Object[] array = list.toArray();
    System.out.println(Arrays.toString(array));  // Output: [Apple, Orange]
    ```

20. **`toArray(T[] a)`**  
    Returns an array containing all elements in the list; the runtime type of the returned array is that of the specified array.
    ```java
    String[] array = list.toArray(new String[0]);
    System.out.println(Arrays.toString(array));  // Output: [Apple, Orange]
    ```

### Example of Using a List in Java

Here’s a simple example of using a `List` and some of its methods:

```java
import java.util.*;

public class ListExample {
    public static void main(String[] args) {
        List<String> list = new ArrayList<>();

        list.add("Apple");
        list.add("Banana");
        list.add(1, "Orange");

        System.out.println("List: " + list);  // Output: List: [Apple, Orange, Banana]

        list.remove("Orange");
        System.out.println("After removing Orange: " + list);  // Output: After removing Orange: [Apple, Banana]

        System.out.println("Size of the list: " + list.size());  // Output: Size of the list: 2

        System.out.println("Element at index 1: " + list.get(1));  // Output: Element at index 1: Banana

        list.clear();
        System.out.println("Is the list empty? " + list.isEmpty());  // Output: Is the list empty? true
    }
}
```

This code demonstrates some of the core operations on a `List`, such as adding, removing, and accessing elements.
