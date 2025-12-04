# Ex 2(c) Deque

## AIM:
To write a Java method to count the number of elements present in a deque.

## Algorithm
1. Start  
2. Create a Deque using an array or Java’s built-in Deque interface.  
3. Define a method count() that takes the deque array as input.  
4. Initialize a counter variable c to store the number of non-zero elements.  
5. Traverse the array from index 0 to MAX-1.  
6. For each element, check if it is non-zero.  
7. If non-zero, increment the counter c.  
8. Return the total count.  
9. End  

## Program:
```
/*
Program to count the number of elements present in the deque
Developed by: Santhosh G
RegisterNumber: 212223240152
*/

class DequeCount {
static final int MAX = 10;

public static int count(int[] arr) {
    int c = 0;
    for (int i = 0; i < MAX; i++) {
        if (arr[i] != 0) {
            c++;
        }
    }
    return c;
}

public static void main(String[] args) {
    int[] deque = new int[MAX];

    // Sample deque elements
    deque[0] = 5;
    deque[1] = 10;
    deque[2] = 15;
    deque[3] = 0;
    deque[4] = 20;

    System.out.println("Number of elements in deque: " + count(deque));
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/b8162aa0-9cf6-4d3b-a7d7-11f18be7c6ed)

## Result:
Thus, the Java program to count the number of elements present in the deque is implemented successfully.
