In Java, the `Map` interface represents a collection that maps keys to values. It's a part of the Java Collections Framework and provides various methods for manipulating mappings.

Here are some common `Map` methods and examples of how to use them, along with an example of iterating through a map.

### Common `Map` Methods

1. **`put(K key, V value)`**: Associates the specified value with the specified key in this map.
2. **`get(Object key)`**: Returns the value to which the specified key is mapped, or `null` if this map contains no mapping for the key.
3. **`remove(Object key)`**: Removes the mapping for a key from this map if it is present.
4. **`containsKey(Object key)`**: Returns `true` if this map contains a mapping for the specified key.
5. **`containsValue(Object value)`**: Returns `true` if this map maps one or more keys to the specified value.
6. **`size()`**: Returns the number of key-value mappings in this map.
7. **`isEmpty()`**: Returns `true` if this map contains no key-value mappings.
8. **`clear()`**: Removes all of the mappings from this map.
9. **`keySet()`**: Returns a `Set` view of the keys contained in this map.
10. **`values()`**: Returns a `Collection` view of the values contained in this map.
11. **`entrySet()`**: Returns a `Set` view of the mappings contained in this map.

### Example Code for Each Method

```java
import java.util.HashMap;
import java.util.Map;
import java.util.Set;
import java.util.Collection;

public class MapExample {
    public static void main(String[] args) {
        // Create a HashMap
        Map<String, Integer> map = new HashMap<>();

        // put() method
        map.put("Apple", 3);
        map.put("Banana", 2);
        map.put("Orange", 5);
        System.out.println("Initial map: " + map);

        // get() method
        Integer value = map.get("Banana");
        System.out.println("Value for 'Banana': " + value);

        // remove() method
        map.remove("Apple");
        System.out.println("Map after removing 'Apple': " + map);

        // containsKey() method
        boolean hasKey = map.containsKey("Orange");
        System.out.println("Map contains key 'Orange': " + hasKey);

        // containsValue() method
        boolean hasValue = map.containsValue(2);
        System.out.println("Map contains value 2: " + hasValue);

        // size() method
        int size = map.size();
        System.out.println("Size of the map: " + size);

        // isEmpty() method
        boolean isEmpty = map.isEmpty();
        System.out.println("Map is empty: " + isEmpty);

        // clear() method
        map.clear();
        System.out.println("Map after clear(): " + map);

        // Add elements back to map
        map.put("Grape", 4);
        map.put("Mango", 6);

        // keySet() method
        Set<String> keys = map.keySet();
        System.out.println("Keys in map: " + keys);

        // values() method
        Collection<Integer> values = map.values();
        System.out.println("Values in map: " + values);

        // entrySet() method
        Set<Map.Entry<String, Integer>> entries = map.entrySet();
        System.out.println("Entries in map: " + entries);
    }
}
```

### Iterating Through a Map

There are several ways to iterate through a `Map` in Java:

1. **Using `entrySet()` with a `for-each` loop:**

```java
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
}
```

2. **Using `keySet()` with a `for-each` loop:**

```java
for (String key : map.keySet()) {
    System.out.println("Key: " + key + ", Value: " + map.get(key));
}
```

3. **Using Java 8's `forEach` method with a lambda expression:**

```java
map.forEach((key, value) -> System.out.println("Key: " + key + ", Value: " + value));
```

4. **Using an `Iterator`:**

```java
Iterator<Map.Entry<String, Integer>> iterator = map.entrySet().iterator();
while (iterator.hasNext()) {
    Map.Entry<String, Integer> entry = iterator.next();
    System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
}
```

### Example of Iterating Through a Map

Here's a complete example that demonstrates different ways to iterate through a map:

```java
import java.util.HashMap;
import java.util.Map;
import java.util.Iterator;

public class MapIterationExample {
    public static void main(String[] args) {
        // Create a HashMap
        Map<String, Integer> map = new HashMap<>();
        map.put("Apple", 3);
        map.put("Banana", 2);
        map.put("Orange", 5);

        // Method 1: Using entrySet() with for-each loop
        System.out.println("Using entrySet() with for-each loop:");
        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
        }

        // Method 2: Using keySet() with for-each loop
        System.out.println("\nUsing keySet() with for-each loop:");
        for (String key : map.keySet()) {
            System.out.println("Key: " + key + ", Value: " + map.get(key));
        }

        // Method 3: Using forEach method (Java 8)
        System.out.println("\nUsing forEach method:");
        map.forEach((key, value) -> System.out.println("Key: " + key + ", Value: " + value));

        // Method 4: Using Iterator
        System.out.println("\nUsing Iterator:");
        Iterator<Map.Entry<String, Integer>> iterator = map.entrySet().iterator();
        while (iterator.hasNext()) {
            Map.Entry<String, Integer> entry = iterator.next();
            System.out.println("Key: " + entry.getKey() + ", Value: " + entry.getValue());
        }
    }
}
```

This code demonstrates different ways to use and iterate over a `Map` in Java.
