The `LinkedHashMap` class in Java is a part of the `java.util` package and extends `HashMap`. It maintains a doubly linked list to preserve the order of entries. Below are some common methods of `LinkedHashMap` along with examples demonstrating their use:

### 1. `put(K key, V value)`

Adds a key-value pair to the map. If the key already exists, it updates the value.

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);
        map.put("Three", 3);

        System.out.println(map);
    }
}
```

### 2. `get(Object key)`

Retrieves the value associated with the specified key.

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        System.out.println("Value for 'One': " + map.get("One"));
    }
}
```

### 3. `remove(Object key)`

Removes the key-value pair associated with the specified key.

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        map.remove("One");
        System.out.println(map);
    }
}
```

### 4. `containsKey(Object key)`

Checks if the map contains a mapping for the specified key.

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        System.out.println("Contains 'One': " + map.containsKey("One"));
        System.out.println("Contains 'Three': " + map.containsKey("Three"));
    }
}
```

### 5. `size()`

Returns the number of key-value pairs in the map.

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        System.out.println("Size of the map: " + map.size());
    }
}
```

### 6. `clear()`

Removes all key-value pairs from the map.

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        map.clear();
        System.out.println("Map after clear: " + map);
    }
}
```

### Iteration Over a LinkedHashMap

To iterate over a `LinkedHashMap`, you can use a variety of methods:

#### 1. Iterating Over Entries

```java
import java.util.LinkedHashMap;
import java.util.Map;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + " = " + entry.getValue());
        }
    }
}
```

#### 2. Iterating Over Keys

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        for (String key : map.keySet()) {
            System.out.println(key + " = " + map.get(key));
        }
    }
}
```

#### 3. Iterating Over Values

```java
import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String, Integer> map = new LinkedHashMap<>();
        map.put("One", 1);
        map.put("Two", 2);

        for (Integer value : map.values()) {
            System.out.println(value);
        }
    }
}
```

These examples cover the basic methods and iteration techniques for `LinkedHashMap`. Feel free to ask if you need more details!
