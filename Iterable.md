# Iterable in Java

In Java, the `Iterable` interface is a part of the Java Collections Framework and is the root interface for collections that can be iterated over. Classes that implement the `Iterable` interface must provide an implementation of the `iterator()` method, which returns an `Iterator` over elements of a specified type.

Here’s a breakdown of the methods available in the `Iterable` interface and the methods of the `Iterator` interface that are commonly used for iteration:

### Methods in the `Iterable` Interface

```java
public interface Iterable<T> {
    // Returns an iterator over elements of type T.
    Iterator<T> iterator();

    // (Since Java 8) Performs the given action for each element of the Iterable until all elements have been processed or the action throws an exception.
    default void forEach(Consumer<? super T> action) {
        Objects.requireNonNull(action);
        for (T t : this) {
            action.accept(t);
        }
    }

    // (Since Java 8) Creates a Spliterator over the elements described by this Iterable.
    default Spliterator<T> spliterator() {
        return Spliterators.spliteratorUnknownSize(iterator(), 0);
    }
}
```

### Methods in the `Iterator` Interface

#### 1. `hasNext()`

- **Purpose**: Returns `true` if the iteration has more elements.
- **Example**:
  ```java
  Iterator<String> iterator = myIterableClass.iterator();
  while (iterator.hasNext()) {
      System.out.println(iterator.next());
  }
  ```

#### 2. `next()`

- **Purpose**: Returns the next element in the iteration.
- **Example**:
  ```java
  String element = iterator.next();
  ```

#### 3. `remove()`

- **Purpose**: Removes from the underlying collection the last element returned by the iterator. This method is optional and is not supported by all `Iterator` implementations.
- **Example**:
  ```java
  iterator.remove();  // Throws UnsupportedOperationException if not supported
  ```

#### 4. `forEachRemaining(Consumer<? super E> action)`

- **Purpose**: Performs the given action for each remaining element in the iteration.
- **Example**:
  ```java
  iterator.forEachRemaining(System.out::println);
  ```

### Example Implementation

Here’s a simple example of a class implementing `Iterable`:

```java
import java.util.*;

public class MyIterableClass implements Iterable<String> {
    private List<String> myList = Arrays.asList("A", "B", "C");

    @Override
    public Iterator<String> iterator() {
        return myList.iterator();
    }

    public static void main(String[] args) {
        MyIterableClass myIterableClass = new MyIterableClass();

        // Using iterator
        Iterator<String> iterator = myIterableClass.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }

        // Using forEach method
        myIterableClass.forEach(System.out::println);

        // Using spliterator
        Spliterator<String> spliterator = myIterableClass.spliterator();
        spliterator.forEachRemaining(System.out::println);
    }
}
```

This example shows how to use `iterator()`, `forEach()`, and `spliterator()` methods. The `Iterator` interface methods like `hasNext()`, `next()`, and `remove()` are also demonstrated.
