Here are some common `HashMap` methods in Java, along with example code for each method:

### 1. Creating a `HashMap`

```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        // Creating a HashMap
        HashMap<String, Integer> map = new HashMap<>();
    }
}
```

### 2. Adding Elements (`put` method)

```java
map.put("Apple", 10);
map.put("Banana", 20);
map.put("Orange", 30);
```

### 3. Accessing Elements (`get` method)

```java
Integer appleCount = map.get("Apple");
System.out.println("Apple count: " + appleCount);  // Output: Apple count: 10
```

### 4. Checking if a Key or Value Exists (`containsKey` and `containsValue` methods)

```java
boolean hasBanana = map.containsKey("Banana");
System.out.println("Map contains Banana: " + hasBanana);  // Output: Map contains Banana: true

boolean hasValue30 = map.containsValue(30);
System.out.println("Map contains value 30: " + hasValue30);  // Output: Map contains value 30: true
```

### 5. Removing Elements (`remove` method)

```java
map.remove("Banana");
System.out.println("Map after removing Banana: " + map);  // Output: Map after removing Banana: {Apple=10, Orange=30}
```

### 6. Checking Size of the HashMap (`size` method)

```java
int size = map.size();
System.out.println("Size of the map: " + size);  // Output: Size of the map: 2
```

### 7. Iterating Over HashMap

- **Using `keySet` and `get` Method**

```java
for (String key : map.keySet()) {
    System.out.println(key + " = " + map.get(key));
}
```

- **Using `entrySet`**

```java
for (HashMap.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey() + " = " + entry.getValue());
}
```

- **Using Java 8 forEach and Lambda**

```java
map.forEach((key, value) -> System.out.println(key + " = " + value));
```

### 8. Replacing Elements (`replace` method)

```java
map.replace("Apple", 50);
System.out.println("Map after replacing Apple: " + map);  // Output: Map after replacing Apple: {Apple=50, Orange=30}
```

### 9. Clearing All Elements (`clear` method)

```java
map.clear();
System.out.println("Map after clearing: " + map);  // Output: Map after clearing: {}
```

### Complete Example Code

```java
import java.util.HashMap;
import java.util.Map;

public class HashMapExample {
    public static void main(String[] args) {
        // Creating a HashMap
        HashMap<String, Integer> map = new HashMap<>();

        // Adding elements
        map.put("Apple", 10);
        map.put("Banana", 20);
        map.put("Orange", 30);

        // Accessing elements
        System.out.println("Apple count: " + map.get("Apple"));

        // Checking if key/value exists
        System.out.println("Map contains Banana: " + map.containsKey("Banana"));
        System.out.println("Map contains value 30: " + map.containsValue(30));

        // Removing an element
        map.remove("Banana");
        System.out.println("Map after removing Banana: " + map);

        // Checking size
        System.out.println("Size of the map: " + map.size());

        // Iterating over the HashMap using entrySet
        for (Map.Entry<String, Integer> entry : map.entrySet()) {
            System.out.println(entry.getKey() + " = " + entry.getValue());
        }

        // Using Java 8 forEach method
        map.forEach((key, value) -> System.out.println(key + " = " + value));

        // Replacing an element
        map.replace("Apple", 50);
        System.out.println("Map after replacing Apple: " + map);

        // Clearing all elements
        map.clear();
        System.out.println("Map after clearing: " + map);
    }
}
```

These examples cover the most common methods used with a `HashMap` in Java, along with different ways to iterate through its entries.
