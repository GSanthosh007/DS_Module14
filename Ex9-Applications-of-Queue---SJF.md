# Ex 2(d) Applications of Queue - SJF

## AIM:
To write a Java program to calculate the Total Waiting Time and Average Waiting Time in the Shortest Job First (SJF) scheduling algorithm.

## Algorithm
1. Start  
2. Read the number of processes n and their burst times into array bt[].  
3. Assign process numbers to array p[] from 1 to n.  
4. Sort the processes based on burst time using selection sort, updating both bt[] and p[].  
5. Compute the waiting time wt[] for each process by summing the burst times of previous processes.  
6. Compute the turnaround time tat[] = bt[] + wt[] for each process.  
7. Compute the average waiting time and average turnaround time.  
8. Display the results in tabular form.  
9. End  

## Program:
```
/*
Program to find the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm.
Developed by: Santhosh G
RegisterNumber: 212223240152
*/

import java.util.Scanner;

public class SJF {
public static void main(String[] args) {
Scanner sc = new Scanner(System.in);

pgsql
Copy code
    int[] bt = new int[20];
    int[] p = new int[20];
    int[] wt = new int[20];
    int[] tat = new int[20];

    int total = 0, n;

    n = sc.nextInt();

    for (int i = 0; i < n; i++) {
        bt[i] = sc.nextInt();
        p[i] = i + 1;
    }

    // Selection sort based on burst time
    for (int i = 0; i < n; i++) {
        int pos = i;
        for (int j = i + 1; j < n; j++) {
            if (bt[j] < bt[pos]) {
                pos = j;
            }
        }

        int temp = bt[i];
        bt[i] = bt[pos];
        bt[pos] = temp;

        temp = p[i];
        p[i] = p[pos];
        p[pos] = temp;
    }

    wt[0] = 0;

    for (int i = 1; i < n; i++) {
        wt[i] = 0;
        for (int j = 0; j < i; j++) {
            wt[i] += bt[j];
        }
        total += wt[i];
    }

    float avg_wt = (float) total / n;
    total = 0;

    System.out.println("Process\tBurst Time\tWaiting Time\tTurnaround Time");

    for (int i = 0; i < n; i++) {
        tat[i] = bt[i] + wt[i];
        total += tat[i];

        System.out.println("p" + p[i] + "\t\t" + bt[i] + "\t\t" + wt[i] + "\t\t" + tat[i]);
    }

    float avg_tat = (float) total / n;

    System.out.println("Average Waiting Time = " + avg_wt);
    System.out.println("Average Turnaround Time = " + avg_tat);

    sc.close();
}
}
```

## Output:
![image](https://github.com/user-attachments/assets/5cecae95-1383-4408-a2be-507b449f0a05)

## Result:
Thus, the Java program to calculate the Total Waiting Time and Average Waiting Time in Shortest Job First scheduling algorithm is implemented successfully.
