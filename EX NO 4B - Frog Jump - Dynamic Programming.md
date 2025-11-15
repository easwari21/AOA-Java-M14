
# EX 4B Frog Jump - Dynamic Programming.
## DATE:24/09/25

## AIM:
To write a Java program to for given constraints.
A Frog Jump 1 or 2 steps at a time.
Problem Statement:

A frog is at the bottom of the stairs with n steps. It can jump either 1 or 2 steps at a time. Write a program to find the number of distinct ways the frog can reach the top (n-th step).

Input Format:

A single integer n (1 ≤ n ≤ 45) – number of steps.
 Output Format:

A single integer – number of distinct ways to reach step n.

## Algorithm

1. Read an integer n representing the number of steps the frog needs to reach.
   
2. If n ≤ 1, return 1 since the frog can reach step 0 or 1 in only one way.
   
3. Create an array dp[] of size n + 1, where dp[i] stores the number of ways to reach the ith step.
   
4. For each step i from 2 to n, computem dp[i] = dp[i - 1] + dp[i - 2]

5.Print the value as the final answer and end the program. 

## Program:
```
Program to implement Reverse a String
Developed by: Easwari M
Register Number:212223240033
```
```
import java.util.Scanner;

public class FrogJump {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        scanner.close();
        System.out.println(countWays(n));
    }

    public static int countWays(int n) {
        if (n <= 1) return 1;
        int[] dp = new int[n + 1];
        dp[0] = 1;
        dp[1] = 1;
        for (int i = 2; i <= n; i++) {
            dp[i] = dp[i - 1] + dp[i - 2];
        }
        return dp[n];
    }
}
```

## Output:
<img width="440" height="203" alt="image" src="https://github.com/user-attachments/assets/08f0798e-a9a5-4b0a-b9cb-89d3e40238bc" />



## Result:
The program successfully implemented and the expected output is verified.
