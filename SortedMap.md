In Java, `SortedMap` is an interface that extends `Map` and provides a map that maintains its entries in ascending key order. `TreeMap` is a common implementation of `SortedMap`.

Here's a summary of some important `SortedMap` methods and examples of how to use them:

### 1. `firstKey()`

**Description:** Returns the first (lowest) key currently in the map.

**Example:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        System.out.println("First key: " + map.firstKey());
    }
}
```

**Output:**

```
First key: Apple
```

### 2. `lastKey()`

**Description:** Returns the last (highest) key currently in the map.

**Example:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        System.out.println("Last key: " + map.lastKey());
    }
}
```

**Output:**

```
Last key: Cherry
```

### 3. `headMap(K toKey)`

**Description:** Returns a view of the portion of this map whose keys are strictly less than `toKey`.

**Example:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        SortedMap<String, Integer> headMap = map.headMap("Cherry");
        System.out.println("Head map: " + headMap);
    }
}
```

**Output:**

```
Head map: {Apple=5, Banana=2}
```

### 4. `tailMap(K fromKey)`

**Description:** Returns a view of the portion of this map whose keys are greater than or equal to `fromKey`.

**Example:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        SortedMap<String, Integer> tailMap = map.tailMap("Banana");
        System.out.println("Tail map: " + tailMap);
    }
}
```

**Output:**

```
Tail map: {Banana=2, Cherry=10}
```

### 5. `subMap(K fromKey, K toKey)`

**Description:** Returns a view of the portion of this map whose keys range from `fromKey`, inclusive, to `toKey`, exclusive.

**Example:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        SortedMap<String, Integer> subMap = map.subMap("Banana", "Cherry");
        System.out.println("Sub map: " + subMap);
    }
}
```

**Output:**

```
Sub map: {Banana=2}
```

### Iterating over `SortedMap`

**Example using `for-each` loop:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        // Iterating using for-each loop
        for (SortedMap.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
```

**Output:**

```
Apple: 5
Banana: 2
Cherry: 10
```

**Example using `forEach` with lambda expression:**

```java
import java.util.SortedMap;
import java.util.TreeMap;

public class SortedMapExample {
    public static void main(String[] args) {
        SortedMap<String, Integer> map = new TreeMap<>();
        map.put("Apple", 5);
        map.put("Banana", 2);
        map.put("Cherry", 10);

        // Iterating using forEach and lambda expression
        map.forEach((key, value) -> System.out.println(key + ": " + value));
    }
}
```

**Output:**

```
Apple: 5
Banana: 2
Cherry: 10
```

These examples should give you a good start with using `SortedMap` in Java. If you have any more questions or need further clarification, feel free to ask!
