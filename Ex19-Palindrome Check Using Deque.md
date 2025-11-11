# Ex19 Palindrome Check Using Deque
## DATE:10/11/25
## AIM:
To design a program that checks whether a given message is a palindrome by removing all non-alphanumeric characters, converting all characters to lowercase, and using a deque data structure for comparison.

## Algorithm
1. Start the program.
2. Read an input string from the user.
3. Remove all non-alphanumeric characters from the string.
4.  Convert all characters to lowercase for uniform comparison.
5.  Create a deque (double-ended queue).
6.  Insert each character of the cleaned string into the deque.
7.   While the deque has more than one element:

Remove one character from the front and one from the rear.

Compare both characters.

If they are not equal, the string is not a palindrome.
8. If all pairs match, the string is a palindrome.
9. Display the result.

## Program:
```
/*
Program to check whether a given message is a palindrome by removing all non-alphanumeric characters.
Developed by: K Dilli babu 
Register Number:  212224110015
*/

import java.util.*;

public class PalindromeUsingDeque {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Read input string
        System.out.print("Enter a message: ");
        String input = sc.nextLine();

        // Remove non-alphanumeric characters and convert to lowercase
        String cleaned = input.replaceAll("[^A-Za-z0-9]", "").toLowerCase();

        // Create a deque
        Deque<Character> deque = new LinkedList<Character>();

        // Add characters to the deque
        for (char c : cleaned.toCharArray()) {
            deque.add(c);
        }

        boolean isPalindrome = true;

        // Compare characters from both ends
        while (deque.size() > 1) {
            if (deque.removeFirst() != deque.removeLast()) {
                isPalindrome = false;
                break;
            }
        }

        // Display result
        if (isPalindrome) {
            System.out.println("The given message IS a palindrome.");
        } else {
            System.out.println("The given message is NOT a palindrome.");
        }
    }
}

```

## Output:


<img width="586" height="111" alt="image" src="https://github.com/user-attachments/assets/412f0845-73ab-4013-a801-db132f13a6f1" />

## Result:
The program successfully removes all non-alphanumeric characters, converts the text to lowercase, and uses a deque to efficiently compare characters from both ends. Hence, it determines whether the string is a palindrome.
