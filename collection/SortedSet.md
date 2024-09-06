`SortedSet` is an interface in Java that extends the `Set` interface and represents a set that maintains its elements in ascending order. The `SortedSet` interface provides several methods for working with sorted sets, such as retrieving the first or last element, getting a subset of elements, and so on.

Here are some commonly used methods of `SortedSet` along with example code for each:

### 1. **Creating a `SortedSet`**

A `SortedSet` can be implemented using the `TreeSet` class, which maintains the elements in their natural ordering or according to a specified comparator.

```java
import java.util.SortedSet;
import java.util.TreeSet;

public class SortedSetExample {
    public static void main(String[] args) {
        // Create a SortedSet of integers
        SortedSet<Integer> sortedSet = new TreeSet<>();

        // Adding elements to the SortedSet
        sortedSet.add(5);
        sortedSet.add(1);
        sortedSet.add(3);
        sortedSet.add(7);
        sortedSet.add(2);

        System.out.println("SortedSet: " + sortedSet); // Output: [1, 2, 3, 5, 7]
    }
}
```

### 2. **`first()` Method**

The `first()` method returns the first (lowest) element in the `SortedSet`.

```java
Integer firstElement = sortedSet.first();
System.out.println("First element: " + firstElement); // Output: 1
```

### 3. **`last()` Method**

The `last()` method returns the last (highest) element in the `SortedSet`.

```java
Integer lastElement = sortedSet.last();
System.out.println("Last element: " + lastElement); // Output: 7
```

### 4. **`headSet(toElement)` Method**

The `headSet(toElement)` method returns a view of the portion of this set whose elements are strictly less than `toElement`.

```java
SortedSet<Integer> headSet = sortedSet.headSet(5);
System.out.println("HeadSet (less than 5): " + headSet); // Output: [1, 2, 3]
```

### 5. **`tailSet(fromElement)` Method**

The `tailSet(fromElement)` method returns a view of the portion of this set whose elements are greater than or equal to `fromElement`.

```java
SortedSet<Integer> tailSet = sortedSet.tailSet(3);
System.out.println("TailSet (greater than or equal to 3): " + tailSet); // Output: [3, 5, 7]
```

### 6. **`subSet(fromElement, toElement)` Method**

The `subSet(fromElement, toElement)` method returns a view of the portion of this set whose elements range from `fromElement`, inclusive, to `toElement`, exclusive.

```java
SortedSet<Integer> subSet = sortedSet.subSet(2, 7);
System.out.println("SubSet (from 2 to 7): " + subSet); // Output: [2, 3, 5]
```

### 7. **`comparator()` Method**

The `comparator()` method returns the comparator used to order the elements in this set, or `null` if this set uses the natural ordering of its elements.

```java
java.util.Comparator<? super Integer> comparator = sortedSet.comparator();
System.out.println("Comparator: " + comparator); // Output: null (if natural ordering is used)
```

### 8. **Iteration Over `SortedSet`**

To iterate over a `SortedSet`, you can use an enhanced for loop, an iterator, or a lambda expression.

#### Using an Enhanced For Loop

```java
for (Integer num : sortedSet) {
    System.out.println(num);
}
```

#### Using an Iterator

```java
java.util.Iterator<Integer> iterator = sortedSet.iterator();
while (iterator.hasNext()) {
    System.out.println(iterator.next());
}
```

#### Using a Lambda Expression

```java
sortedSet.forEach(System.out::println);
```

### Example Program

Here's a full example demonstrating all of the methods discussed:

```java
import java.util.SortedSet;
import java.util.TreeSet;

public class SortedSetExample {
    public static void main(String[] args) {
        // Create a SortedSet of integers
        SortedSet<Integer> sortedSet = new TreeSet<>();

        // Adding elements to the SortedSet
        sortedSet.add(5);
        sortedSet.add(1);
        sortedSet.add(3);
        sortedSet.add(7);
        sortedSet.add(2);

        System.out.println("SortedSet: " + sortedSet);

        // first() method
        Integer firstElement = sortedSet.first();
        System.out.println("First element: " + firstElement);

        // last() method
        Integer lastElement = sortedSet.last();
        System.out.println("Last element: " + lastElement);

        // headSet(toElement) method
        SortedSet<Integer> headSet = sortedSet.headSet(5);
        System.out.println("HeadSet (less than 5): " + headSet);

        // tailSet(fromElement) method
        SortedSet<Integer> tailSet = sortedSet.tailSet(3);
        System.out.println("TailSet (greater than or equal to 3): " + tailSet);

        // subSet(fromElement, toElement) method
        SortedSet<Integer> subSet = sortedSet.subSet(2, 7);
        System.out.println("SubSet (from 2 to 7): " + subSet);

        // comparator() method
        java.util.Comparator<? super Integer> comparator = sortedSet.comparator();
        System.out.println("Comparator: " + comparator);

        // Iteration over SortedSet using enhanced for loop
        System.out.println("Iterating using enhanced for loop:");
        for (Integer num : sortedSet) {
            System.out.println(num);
        }

        // Iteration using Iterator
        System.out.println("Iterating using Iterator:");
        java.util.Iterator<Integer> iterator = sortedSet.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        // Iteration using lambda expression
        System.out.println("Iterating using lambda expression:");
        sortedSet.forEach(System.out::println);
    }
}
```

This example demonstrates the various methods and how to use them to manipulate and iterate over a `SortedSet`.
