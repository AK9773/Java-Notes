Here’s a basic implementation of a `HashTable` in Java with methods and iteration examples. The `HashTable` class will include common operations like `put`, `get`, `remove`, `containsKey`, and `size`. Additionally, I'll include an iteration method to traverse the table.

```java
import java.util.*;

public class SimpleHashTable<K, V> {
    private static final int INITIAL_CAPACITY = 16;
    private List<Entry<K, V>>[] table;
    private int size = 0;

    public SimpleHashTable() {
        table = new ArrayList[INITIAL_CAPACITY];
        for (int i = 0; i < table.length; i++) {
            table[i] = new ArrayList<>();
        }
    }

    private static class Entry<K, V> {
        K key;
        V value;

        Entry(K key, V value) {
            this.key = key;
            this.value = value;
        }
    }

    private int getBucketIndex(K key) {
        return key == null ? 0 : key.hashCode() % table.length;
    }

    public void put(K key, V value) {
        int index = getBucketIndex(key);
        List<Entry<K, V>> bucket = table[index];
        for (Entry<K, V> entry : bucket) {
            if (entry.key.equals(key)) {
                entry.value = value;
                return;
            }
        }
        bucket.add(new Entry<>(key, value));
        size++;
    }

    public V get(K key) {
        int index = getBucketIndex(key);
        List<Entry<K, V>> bucket = table[index];
        for (Entry<K, V> entry : bucket) {
            if (entry.key.equals(key)) {
                return entry.value;
            }
        }
        return null;
    }

    public void remove(K key) {
        int index = getBucketIndex(key);
        List<Entry<K, V>> bucket = table[index];
        Iterator<Entry<K, V>> iterator = bucket.iterator();
        while (iterator.hasNext()) {
            Entry<K, V> entry = iterator.next();
            if (entry.key.equals(key)) {
                iterator.remove();
                size--;
                return;
            }
        }
    }

    public boolean containsKey(K key) {
        int index = getBucketIndex(key);
        List<Entry<K, V>> bucket = table[index];
        for (Entry<K, V> entry : bucket) {
            if (entry.key.equals(key)) {
                return true;
            }
        }
        return false;
    }

    public int size() {
        return size;
    }

    // Iteration method
    public void iterate() {
        for (List<Entry<K, V>> bucket : table) {
            for (Entry<K, V> entry : bucket) {
                System.out.println("Key: " + entry.key + ", Value: " + entry.value);
            }
        }
    }

    public static void main(String[] args) {
        SimpleHashTable<String, Integer> hashTable = new SimpleHashTable<>();

        // Putting values
        hashTable.put("One", 1);
        hashTable.put("Two", 2);
        hashTable.put("Three", 3);

        // Getting values
        System.out.println("Value for 'Two': " + hashTable.get("Two"));

        // Removing a value
        hashTable.remove("Two");
        System.out.println("Contains 'Two': " + hashTable.containsKey("Two"));

        // Iterating over the table
        System.out.println("HashTable contents:");
        hashTable.iterate();
    }
}
```

### Explanation:

1. **Initialization**: The `SimpleHashTable` class initializes with a fixed capacity and uses an `ArrayList` for each bucket to handle collisions.
2. **put()**: Adds a key-value pair to the table, updating the value if the key already exists.
3. **get()**: Retrieves the value associated with a key.
4. **remove()**: Removes a key-value pair based on the key.
5. **containsKey()**: Checks if a key exists in the table.
6. **size()**: Returns the number of key-value pairs in the table.
7. **iterate()**: Iterates through all the entries in the table and prints them.

You can modify and expand this basic implementation based on your needs, such as handling resizing or adding more sophisticated collision resolution techniques.
