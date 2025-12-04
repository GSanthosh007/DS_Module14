# Ex2(A) Dequeue Elements from Circular Queue
## DATE:06-09-2025

## AIM:
To write a Java program to delete three elements from a filled circular queue.

## Algorithm
1.	Start
2.	Define a circular queue using an integer array of fixed size SIZE and initialize front and rear to -1.
3.	Define the deQueue() method to remove and return an element from the front of the circular queue.
4.	Check if the queue is empty using isEmpty(); if empty, display an appropriate message.
5.	If the queue contains only one element, reset both front and rear to -1.
6.	If more elements exist, update the front pointer using modulo operation ((front + 1) % SIZE).
7.	Return the removed element.
8.	End

## Program:
```
/*
Program to delete three elements from the filled circular queue
Developed by: Santhosh G
RegisterNumber: 212223240152
*/

class CircularQueue {
static final int SIZE = 5;
int[] items = new int[SIZE];
int front = -1, rear = -1;

boolean isEmpty() {
    return front == -1;
}

int deQueue() {
    if (isEmpty()) {
        System.out.println("Queue is Empty!!");
        return -1;
    }

    int element = items[front];

    if (front == rear) {
        front = -1;
        rear = -1;
    } else {
        front = (front + 1) % SIZE;
    }
    return element;
}
}

public class Main {
public static void main(String[] args) {
CircularQueue cq = new CircularQueue();

pgsql
Copy code
    // Pre-filled circular queue
    cq.items[0] = 10;
    cq.items[1] = 20;
    cq.items[2] = 30;
    cq.items[3] = 40;
    cq.items[4] = 50;
    cq.front = 0;
    cq.rear = 4;

    System.out.println("Deleted Elements:");
    System.out.println(cq.deQueue());
    System.out.println(cq.deQueue());
    System.out.println(cq.deQueue());
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/c7182b0c-6d03-4252-8a4a-0617ebf540ef)

## Result:
Thus, the Java program to delete three elements from the filled circular queue is implemented successfully.






