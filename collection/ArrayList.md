# ArrayList in Java

Here's a list of common `ArrayList` methods and properties in Java with one-line explanations and example code for each:

### 1. `add(E e)`

**Explanation:** Appends the specified element to the end of the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
```

### 2. `add(int index, E element)`

**Explanation:** Inserts the specified element at the specified position in the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add(0, "Banana");
```

### 3. `remove(int index)`

**Explanation:** Removes the element at the specified position in the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.remove(0);
```

### 4. `remove(Object o)`

**Explanation:** Removes the first occurrence of the specified element from the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
list.remove("Banana");
```

### 5. `get(int index)`

**Explanation:** Returns the element at the specified position in the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
String fruit = list.get(0);
```

### 6. `set(int index, E element)`

**Explanation:** Replaces the element at the specified position in the list with the specified element.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.set(0, "Banana");
```

### 7. `size()`

**Explanation:** Returns the number of elements in the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
int size = list.size();
```

### 8. `clear()`

**Explanation:** Removes all elements from the list.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.clear();
```

### 9. `contains(Object o)`

**Explanation:** Returns `true` if the list contains the specified element.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
boolean hasApple = list.contains("Apple");
```

### 10. `indexOf(Object o)`

**Explanation:** Returns the index of the first occurrence of the specified element, or `-1` if not found.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
int index = list.indexOf("Apple");
```

### 11. `isEmpty()`

**Explanation:** Returns `true` if the list contains no elements.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
boolean empty = list.isEmpty();
```

### 12. `toArray()`

**Explanation:** Returns an array containing all elements in the list in proper sequence.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
Object[] array = list.toArray();
```

### 13. `subList(int fromIndex, int toIndex)`

**Explanation:** Returns a view of the portion of this list between the specified indices.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
List<String> subList = list.subList(0, 1);
```

### 14. `ensureCapacity(int minCapacity)`

**Explanation:** Increases the capacity of the `ArrayList` to ensure it can hold at least the specified number of elements.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.ensureCapacity(20);
```

### 15. `trimToSize()`

**Explanation:** Trims the capacity of the `ArrayList` to be the list's current size.  
**Example:**

```java
ArrayList<String> list = new ArrayList<>();
list.add("Apple");
list.trimToSize();
```

These methods and properties cover most of the common operations you can perform on an `ArrayList`.
