Here are some examples of commonly used `HashSet` methods in Java, along with an example of how to iterate over a `HashSet`.

### 1. **Creating a HashSet**

First, let's create a `HashSet` and add some elements to it:

```java
import java.util.HashSet;

public class HashSetExample {
    public static void main(String[] args) {
        // Create a HashSet
        HashSet<String> fruits = new HashSet<>();

        // Adding elements to the HashSet
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");
        fruits.add("Mango");

        System.out.println("HashSet: " + fruits);
    }
}
```

### 2. **Common HashSet Methods**

#### a. **`add(E e)`**: Adds the specified element to the set if it is not already present.

```java
fruits.add("Grapes");  // Adds "Grapes" to the set
```

#### b. **`remove(Object o)`**: Removes the specified element from the set, if it is present.

```java
fruits.remove("Banana");  // Removes "Banana" from the set
```

#### c. **`contains(Object o)`**: Returns `true` if the set contains the specified element.

```java
boolean hasApple = fruits.contains("Apple");  // Checks if "Apple" is present
System.out.println("Contains Apple? " + hasApple);
```

#### d. **`isEmpty()`**: Returns `true` if the set contains no elements.

```java
boolean isEmpty = fruits.isEmpty();  // Checks if the set is empty
System.out.println("Is HashSet empty? " + isEmpty);
```

#### e. **`size()`**: Returns the number of elements in the set.

```java
int size = fruits.size();  // Gets the size of the set
System.out.println("Size of HashSet: " + size);
```

#### f. **`clear()`**: Removes all elements from the set.

```java
fruits.clear();  // Clears the HashSet
System.out.println("HashSet after clear: " + fruits);
```

### 3. **Iterating Over a HashSet**

You can iterate over a `HashSet` using different methods, such as using a `for-each` loop or an `Iterator`.

#### a. **Using a `for-each` loop**

```java
for (String fruit : fruits) {
    System.out.println(fruit);
}
```

#### b. **Using an `Iterator`**

```java
import java.util.Iterator;

Iterator<String> iterator = fruits.iterator();
while (iterator.hasNext()) {
    String fruit = iterator.next();
    System.out.println(fruit);
}
```

### Complete Example Code

Here's a complete example demonstrating all the methods and iterations:

```java
import java.util.HashSet;
import java.util.Iterator;

public class HashSetExample {
    public static void main(String[] args) {
        // Create a HashSet
        HashSet<String> fruits = new HashSet<>();

        // Adding elements to the HashSet
        fruits.add("Apple");
        fruits.add("Banana");
        fruits.add("Orange");
        fruits.add("Mango");

        System.out.println("HashSet: " + fruits);

        // Remove an element
        fruits.remove("Banana");
        System.out.println("After removing Banana: " + fruits);

        // Check if an element exists
        boolean hasApple = fruits.contains("Apple");
        System.out.println("Contains Apple? " + hasApple);

        // Get the size of the HashSet
        int size = fruits.size();
        System.out.println("Size of HashSet: " + size);

        // Check if HashSet is empty
        boolean isEmpty = fruits.isEmpty();
        System.out.println("Is HashSet empty? " + isEmpty);

        // Iterate using for-each loop
        System.out.println("Iterating using for-each loop:");
        for (String fruit : fruits) {
            System.out.println(fruit);
        }

        // Iterate using Iterator
        System.out.println("Iterating using Iterator:");
        Iterator<String> iterator = fruits.iterator();
        while (iterator.hasNext()) {
            String fruit = iterator.next();
            System.out.println(fruit);
        }

        // Clear the HashSet
        fruits.clear();
        System.out.println("HashSet after clear: " + fruits);
    }
}
```

This example demonstrates how to use various `HashSet` methods and how to iterate over a `HashSet` in Java.
