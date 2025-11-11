# Ex17 Reversing a String Using Stack Data Structure
## DATE:10/11/25
## AIM:
To write a Java program that reverses an input string using a stack, without using built-in reverse functions.

## Algorithm
1. Start the program.
2. Read the input string from the user.
3. Create an empty stack of characters
4.  Traverse the string and push each character onto the stack.
5.  Pop each character from the stack and append it to a new string — this gives the reversed string.
6.  Display the reversed string.
7.   Stop the program.

## Program:
```
/*
Program to reverse an input string using a stack.
Developed by: K DIlli babu
Register Number:  212224110015
*/

import java.util.*;

public class ReverseStringUsingStack {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read input from user
        System.out.print("Enter a string: ");
        String input = sc.nextLine();

        // Create a stack
        Stack<Character> stack = new Stack<Character>();

        // Push all characters of string into stack
        for (char ch : input.toCharArray()) {
            stack.push(ch);
        }

        // Pop all characters to get reversed string
        String reversed = "";
        while (!stack.isEmpty()) {
            reversed += stack.pop();
        }

        // Display reversed string
        System.out.println("Reversed string: " + reversed);
    }
}

```

## Output:


<img width="620" height="130" alt="image" src="https://github.com/user-attachments/assets/001a59bd-714d-49e2-af5d-c52cb4f88629" />

## Result:
Thus, the program successfully reverses the given string using a stack without relying on built-in reverse functions.
