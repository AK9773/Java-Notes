# Stack in Java

Here's a list of commonly used methods from the `Stack` class in Java, along with a one-line explanation and example code for each:

### 1. **`push(E item)`**

Adds an element to the top of the stack.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(10); // Adds 10 to the stack
        System.out.println("After push: " + stack); // Output: [10]
    }
}
```

### 2. **`pop()`**

Removes and returns the element at the top of the stack.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(20);
        int top = stack.pop(); // Removes and returns 20
        System.out.println("After pop: " + stack); // Output: []
        System.out.println("Popped element: " + top); // Output: 20
    }
}
```

### 3. **`peek()`**

Returns the element at the top of the stack without removing it.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(30);
        int top = stack.peek(); // Returns 30 without removing
        System.out.println("Top element: " + top); // Output: 30
        System.out.println("Stack after peek: " + stack); // Output: [30]
    }
}
```

### 4. **`isEmpty()`**

Checks if the stack is empty.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        boolean empty = stack.isEmpty(); // Returns true
        System.out.println("Is stack empty? " + empty); // Output: true
    }
}
```

### 5. **`search(Object o)`**

Returns the 1-based position from the top of the stack where the object is located, or `-1` if not found.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(40);
        stack.push(50);
        int position = stack.search(40); // Returns 2 (1-based position from the top)
        System.out.println("Position of 40: " + position); // Output: 2
    }
}
```

### 6. **`size()`**

Returns the number of elements in the stack.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(60);
        stack.push(70);
        int size = stack.size(); // Returns 2
        System.out.println("Stack size: " + size); // Output: 2
    }
}
```

### 7. **`clear()`**

Removes all elements from the stack.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(80);
        stack.push(90);
        stack.clear(); // Clears all elements
        System.out.println("Stack after clear: " + stack); // Output: []
    }
}
```

### 8. **`toString()`**

Returns a string representation of the stack.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(100);
        stack.push(110);
        System.out.println("Stack contents: " + stack.toString()); // Output: [100, 110]
    }
}
```

### 9. **`contains(Object o)`**

Checks if the stack contains a specific element.

```java
import java.util.Stack;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(120);
        boolean contains = stack.contains(120); // Returns true
        System.out.println("Does stack contain 120? " + contains); // Output: true
    }
}
```

### 10. **`iterator()`**

Returns an iterator over the elements in the stack in proper sequence.

```java
import java.util.Stack;
import java.util.Iterator;

public class StackExample {
    public static void main(String[] args) {
        Stack<Integer> stack = new Stack<>();
        stack.push(130);
        stack.push(140);

        Iterator<Integer> iterator = stack.iterator();
        System.out.print("Stack elements: ");
        while (iterator.hasNext()) {
            System.out.print(iterator.next() + " "); // Output: 130 140
        }
    }
}
```

These methods provide the basic functionality needed to operate on a stack in Java. If you have more specific use cases or need further details, feel free to ask!
