# Ex18 Simulation of a Ticket Counter Using Queue (Linked List Implementation)
## DATE:10/11/25
## AIM:
To simulate the functioning of a ticket counter that operates on a First-In-First-Out (FIFO) basis using a queue implemented via a linked list in Java.
## Algorithm
1. Start the program.
2. Create a Queue using the LinkedList class
3. Enqueue (add) customers to the queue as they arrive
4. Display the current queue of customers
5. Dequeue (remove) customers from the queue one by one as they are served.
6.  Display which customer is being served and the remaining queue.
7.   Repeat until all customers are served.

## Program:
```
/*
Program to simulate the functioning of a ticket counter that operates on a First-In-First-Out (FIFO) basis
using a queue implemented via a linked list.
Developed by: K Dilli babu
Register Number:  212224110015
*/

import java.util.*;

public class TicketCounterSimulation {
    public static void main(String[] args) {
        // Create a queue using LinkedList
        Queue<String> queue = new LinkedList<String>();

        // Add customers to the queue
        queue.add("Customer 1");
        queue.add("Customer 2");
        queue.add("Customer 3");
        queue.add("Customer 4");

        System.out.println("Initial Queue: " + queue);

        // Serve customers one by one
        while (!queue.isEmpty()) {
            String served = queue.poll(); // removes the head of the queue
            System.out.println(served + " is being served.");
            System.out.println("Remaining Queue: " + queue);
            System.out.println();
        }

        System.out.println("All customers have been served!");
    }
}

```

## Output:

<img width="651" height="399" alt="image" src="https://github.com/user-attachments/assets/80344af2-0e98-41f4-9222-90cd65c779bf" />


## Result:
Thus, the program successfully simulates a ticket counter queue where customers are served in FIFO order using a linked list-based queue implementation.
