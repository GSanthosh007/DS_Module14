# Ex 2(b) Priority Queue

## AIM:
To write a Java program to display the elements of a priority queue after insertion and deletion operations.

## Algorithm
1. Start  
2. Create a PriorityQueue and insert elements into it.  
3. Define a method printQueue() to display all elements of the priority queue.  
4. Use a loop to print each element retrieved from the queue (by converting to an array).  
5. Perform deletion using poll() operation.  
6. Display the queue elements after insertion and deletion.  
7. End.

## Program:
```
/*
Program to display the elements of the priority queue after insertion and deletion operation
Developed by: Santhosh G
RegisterNumber: 212223240152
*/

import java.util.PriorityQueue;

public class Main {

pgsql
Copy code
public static void printQueue(PriorityQueue<Integer> pq) {
    Object[] arr = pq.toArray();
    for (Object num : arr) {
        System.out.print(num + " ");
    }
    System.out.println();
}

public static void main(String[] args) {
    PriorityQueue<Integer> pq = new PriorityQueue<>();

    // Insert elements
    pq.add(30);
    pq.add(10);
    pq.add(50);
    pq.add(20);

    System.out.println("Priority Queue after insertion:");
    printQueue(pq);

    // Deletion (removing the highest priority element)
    pq.poll();
    pq.poll();

    System.out.println("Priority Queue after deletion:");
    printQueue(pq);
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/20fc64fc-3df1-45f9-bc0f-c52565598478)

## Result:
Thus, the Java program to display the elements of the priority queue after insertion and deletion operations is implemented successfully.
