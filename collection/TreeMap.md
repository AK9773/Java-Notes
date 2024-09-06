`TreeMap` is a part of the Java Collections Framework and implements the `NavigableMap` interface. It is a Red-Black tree-based implementation of the `SortedMap` interface. Here are some common methods of `TreeMap` along with examples for each:

### 1. **`put(K key, V value)`**

Adds a key-value pair to the `TreeMap`. If the key already exists, it updates the value associated with that key.

```java
import java.util.TreeMap;

public class TreeMapPutExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        System.out.println(map);
    }
}
```

### 2. **`get(Object key)`**

Returns the value associated with the specified key. If the key does not exist, it returns `null`.

```java
import java.util.TreeMap;

public class TreeMapGetExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        System.out.println("Value for 'Banana': " + map.get("Banana"));
    }
}
```

### 3. **`remove(Object key)`**

Removes the entry for the specified key if it is present.

```java
import java.util.TreeMap;

public class TreeMapRemoveExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        map.remove("Banana");
        System.out.println(map);
    }
}
```

### 4. **`firstKey()`**

Returns the first (lowest) key currently in the map.

```java
import java.util.TreeMap;

public class TreeMapFirstKeyExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        System.out.println("First key: " + map.firstKey());
    }
}
```

### 5. **`lastKey()`**

Returns the last (highest) key currently in the map.

```java
import java.util.TreeMap;

public class TreeMapLastKeyExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        System.out.println("Last key: " + map.lastKey());
    }
}
```

### 6. **`keySet()`**

Returns a `Set` view of the keys contained in the map.

```java
import java.util.Set;
import java.util.TreeMap;

public class TreeMapKeySetExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        Set<String> keys = map.keySet();
        System.out.println("Keys: " + keys);
    }
}
```

### 7. **`values()`**

Returns a `Collection` view of the values contained in the map.

```java
import java.util.Collection;
import java.util.TreeMap;

public class TreeMapValuesExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        Collection<Integer> values = map.values();
        System.out.println("Values: " + values);
    }
}
```

### 8. **Iteration using `for-each` loop**

You can iterate over the entries of the `TreeMap` using a `for-each` loop.

```java
import java.util.Map;
import java.util.TreeMap;

public class TreeMapIterationExample {
    public static void main(String[] args) {
        TreeMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Cherry", 30);

        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

These examples cover the basic operations you can perform with a `TreeMap`. If you have any specific scenarios or need more advanced operations, feel free to ask!
