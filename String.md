When you create a String with literal (e.g. String str = "Hello";) the Object is not created in Heap it will be available in StringPool only, however when you create a String using 'new' operator (e.g. String str = new String ("Hello")) then the Object in StringPool is created along with one more object in Heap.

Below are examples of some common `String` methods and an iteration method in Java.

### String Methods

1. **`length()`**: Returns the length of the string.

   ```java
   String str = "Hello, World!";
   int length = str.length();
   System.out.println("Length: " + length); // Output: Length: 13
   ```

2. **`charAt(int index)`**: Returns the character at the specified index.

   ```java
   String str = "Hello, World!";
   char ch = str.charAt(7);
   System.out.println("Character at index 7: " + ch); // Output: Character at index 7: W
   ```

3. **`substring(int beginIndex, int endIndex)`**: Returns a substring from `beginIndex` to `endIndex - 1`.

   ```java
   String str = "Hello, World!";
   String substr = str.substring(7, 12);
   System.out.println("Substring: " + substr); // Output: Substring: World
   ```

4. **`toLowerCase()`**: Converts all characters in the string to lowercase.

   ```java
   String str = "Hello, World!";
   String lower = str.toLowerCase();
   System.out.println("Lowercase: " + lower); // Output: Lowercase: hello, world!
   ```

5. **`toUpperCase()`**: Converts all characters in the string to uppercase.

   ```java
   String str = "Hello, World!";
   String upper = str.toUpperCase();
   System.out.println("Uppercase: " + upper); // Output: Uppercase: HELLO, WORLD!
   ```

6. **`trim()`**: Removes leading and trailing whitespace.

   ```java
   String str = "   Hello, World!   ";
   String trimmed = str.trim();
   System.out.println("Trimmed: '" + trimmed + "'"); // Output: Trimmed: 'Hello, World!'
   ```

7. **`replace(CharSequence target, CharSequence replacement)`**: Replaces occurrences of the target sequence with the replacement sequence.

   ```java
   String str = "Hello, World!";
   String replaced = str.replace("World", "Java");
   System.out.println("Replaced: " + replaced); // Output: Replaced: Hello, Java!
   ```

8. **`contains(CharSequence sequence)`**: Checks if the string contains the specified sequence.

   ```java
   String str = "Hello, World!";
   boolean contains = str.contains("World");
   System.out.println("Contains 'World': " + contains); // Output: Contains 'World': true
   ```

9. **`split(String regex)`**: Splits the string around matches of the given regular expression.

   ```java
   String str = "apple,banana,orange";
   String[] fruits = str.split(",");
   for (String fruit : fruits) {
       System.out.println(fruit);
   }
   // Output:
   // apple
   // banana
   // orange
   ```

10. **`indexOf(String str)`**: Returns the index of the first occurrence of the specified substring.
    ```java
    String str = "Hello, World!";
    int index = str.indexOf("World");
    System.out.println("Index of 'World': " + index); // Output: Index of 'World': 7
    ```

### Iteration Over a String

You can iterate over the characters of a string using a `for` loop:

```java
String str = "Hello, World!";
for (int i = 0; i < str.length(); i++) {
    char ch = str.charAt(i);
    System.out.println(ch);
}
```

Or using an enhanced `for` loop with `toCharArray()`:

```java
String str = "Hello, World!";
for (char ch : str.toCharArray()) {
    System.out.println(ch);
}
```

Both methods will print each character of the string on a new line.
