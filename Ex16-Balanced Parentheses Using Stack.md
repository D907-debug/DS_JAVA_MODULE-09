# Ex16 Check for Balanced Parentheses Using Stack
## DATE:23/10/25
## AIM:
To write a Java program that verifies whether the parentheses (brackets) in an input string are balanced — meaning each opening bracket (, {, [ has a corresponding and correctly ordered closing bracket ), }, ].

## Algorithm
1. Start the program.
2. Read an input string containing parentheses/brackets.
3. Create a stack to store opening brackets.
4.  Traverse each character of the string:

If the character is an opening bracket ((, {, [), push it onto the stack.

If it is a closing bracket (), }, ]):

Check if the stack is empty → if yes, it’s unbalanced.

Otherwise, pop the top element from the stack and verify if it matches the current closing bracket.

If not matching → unbalanced.
5.   After traversal, if the stack is empty, the string is balanced; otherwise, it’s unbalanced.

Display the result.

End the program.

## Program:
```
/*
Program to verify whether the parentheses (brackets) in an input string are balanced
Developed by: Dilli babu K
RegisterNumber: 212224110015
*/

import java.util.*;

public class BalancedParentheses {
    public static boolean isBalanced(String expr) {
        Stack<Character> stack = new Stack<>();

        for (char ch : expr.toCharArray()) {
            if (ch == '(' || ch == '{' || ch == '[') {
                stack.push(ch);
            } else if (ch == ')' || ch == '}' || ch == ']') {
                if (stack.isEmpty()) {
                    return false;
                }

                char top = stack.pop();
                if ((ch == ')' && top != '(') ||
                    (ch == '}' && top != '{') ||
                    (ch == ']' && top != '[')) {
                    return false;
                }
            }
        }

        return stack.isEmpty();
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter an expression: ");
        String expression = sc.nextLine();

        if (isBalanced(expression))
            System.out.println("The parentheses are balanced.");
        else
            System.out.println("The parentheses are NOT balanced.");

        sc.close();
    }
}

```

## Output:
<img width="579" height="104" alt="image" src="https://github.com/user-attachments/assets/4b297ae6-7a5a-4a29-b062-9cdc9fa1e511" />



## Result:
Thus,the program correctly checks whether an input string has balanced parentheses using a stack.
