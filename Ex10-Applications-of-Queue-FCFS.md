# Ex 2(e) Applications of Queue – FCFS

## AIM:
To write a Java function to calculate the turnaround time of each process given their burst time and waiting time in the First Come First Serve scheduling algorithm.

## Algorithm
1. Start with process, burst time, and waiting time arrays.  
2. Loop through each process from i = 0 to n-1.  
3. Compute `tat[i] = burst_time[i] + wait_time[i]`.  
4. End the algorithm.

## Program:
```
/*
Program to calculate turnaround time of each process using FCFS
Developed by: Santhosh G
RegisterNumber: 212223240152
*/

public class FCFS_Turnaround {

    // Function to calculate turnaround time
    public static void turnaroundTime(int[] proc, int n, int[] burst_time, int[] wait_time, int[] tat) {
        for (int i = 0; i < n; i++) {
            tat[i] = burst_time[i] + wait_time[i];
        }
    }

    public static void main(String[] args) {
        int[] proc = {1, 2, 3};
        int[] burst_time = {5, 9, 6};
        int[] wait_time = {0, 5, 14};
        int n = proc.length;
        int[] tat = new int[n];

        turnaroundTime(proc, n, burst_time, wait_time, tat);

        System.out.println("Process\tBurst Time\tWait Time\tTurnaround Time");
        for (int i = 0; i < n; i++) {
            System.out.println(proc[i] + "\t\t" + burst_time[i] + "\t\t" + wait_time[i] + "\t\t" + tat[i]);
        }
    }
}
```
Output:

![image](https://github.com/user-attachments/assets/78a4a748-2f69-4465-abe2-69350865f76b)


Result:

Thus, the Java program to calculate the turnaround time of each process given their burst time and waiting time in the First Come First Serve scheduling algorithm is implemented successfully.
