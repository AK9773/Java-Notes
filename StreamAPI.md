Here is an example of the Stream API in Java, demonstrating some of the main methods:

### 1. **`filter()`**

Filters elements based on a condition.

```java
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5, 6, 7, 8, 9);
        List<Integer> evenNumbers = numbers.stream()
                                            .filter(n -> n % 2 == 0) // Filter even numbers
                                            .collect(Collectors.toList());
        System.out.println(evenNumbers); // Output: [2, 4, 6, 8]
    }
}
```

### 2. **`map()`**

Transforms each element in the stream.

```java
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5);
        List<Integer> squares = numbers.stream()
                                        .map(n -> n * n) // Square each number
                                        .collect(Collectors.toList());
        System.out.println(squares); // Output: [1, 4, 9, 16, 25]
    }
}
```

### 3. **`sorted()`**

Sorts the elements of the stream.

```java
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<String> names = List.of("John", "Alice", "Bob", "David");
        List<String> sortedNames = names.stream()
                                         .sorted() // Sort in natural order
                                         .collect(Collectors.toList());
        System.out.println(sortedNames); // Output: [Alice, Bob, David, John]
    }
}
```

### 4. **`forEach()`**

Performs an action for each element in the stream.

```java
import java.util.List;

public class StreamExample {
    public static void main(String[] args) {
        List<String> names = List.of("John", "Alice", "Bob", "David");
        names.stream()
             .forEach(System.out::println); // Print each name
    }
}
```

### 5. **`collect()`**

Converts the stream into a different form, like a `List`, `Set`, etc.

```java
import java.util.List;
import java.util.Set;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 4, 5);
        Set<Integer> uniqueNumbers = numbers.stream()
                                             .collect(Collectors.toSet()); // Convert to Set
        System.out.println(uniqueNumbers); // Output: [1, 2, 3, 4, 5]
    }
}
```

### 6. **`reduce()`**

Combines elements of the stream into a single result.

```java
import java.util.List;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5);
        int sum = numbers.stream()
                         .reduce(0, (a, b) -> a + b); // Sum all numbers
        System.out.println(sum); // Output: 15
    }
}
```

### 7. **`distinct()`**

Removes duplicate elements from the stream.

```java
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 2, 3, 4, 4, 5);
        List<Integer> distinctNumbers = numbers.stream()
                                                .distinct() // Remove duplicates
                                                .collect(Collectors.toList());
        System.out.println(distinctNumbers); // Output: [1, 2, 3, 4, 5]
    }
}
```

### 8. **`limit()`**

Limits the number of elements in the stream.

```java
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5, 6, 7, 8, 9);
        List<Integer> limitedNumbers = numbers.stream()
                                               .limit(3) // Get only first 3 numbers
                                               .collect(Collectors.toList());
        System.out.println(limitedNumbers); // Output: [1, 2, 3]
    }
}
```

### 9. **`skip()`**

Skips the first n elements of the stream.

```java
import java.util.List;
import java.util.stream.Collectors;

public class StreamExample {
    public static void main(String[] args) {
        List<Integer> numbers = List.of(1, 2, 3, 4, 5, 6, 7, 8, 9);
        List<Integer> skippedNumbers = numbers.stream()
                                               .skip(5) // Skip first 5 numbers
                                               .collect(Collectors.toList());
        System.out.println(skippedNumbers); // Output: [6, 7, 8, 9]
    }
}
```

These examples demonstrate various operations you can perform using Java's Stream API. Let me know if you'd like further details!
