```java


    public class StringBuilderExample {
        public static void main(String[] args) {
            // Step 1: Create a StringBuilder object with "Hello"
            StringBuilder sb = new StringBuilder("Hello");
            System.out.println("Initial string: " + sb); // Output: Hello

            // Step 2: Append ", World!" to the end of "Hello"
            sb.append(", World!");
            System.out.println("After append: " + sb);  // Output: Hello, World!

            // Step 3: Insert " Java" at index 5 (after "Hello")
            sb.insert(5, " Java");
            System.out.println("After insert: " + sb);  // Output: Hello Java, World!

            // Step 4: Delete the substring from index 5 to 10 (exclusive), removing " Java"
            sb.delete(5, 10);
            System.out.println("After delete: " + sb);  // Output: Hello, World!

            // Step 5: Reverse the string
            sb.reverse();
            System.out.println("After reverse: " + sb);  // Output: !dlroW ,olleH

            // Step 6: Convert the StringBuilder to a String
            String finalString = sb.toString();
            System.out.println("Final string: " + finalString);  // Output: !dlroW ,olleH
        }
    }

'''
```
