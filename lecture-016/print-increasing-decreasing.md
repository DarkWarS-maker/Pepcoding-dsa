# Print Increasing Decreasing

> 1. You are given a positive number n. 
> 2. You are required to print the counting from n to 1 and back to n again.
> 3. You are required to not use any loops. Complete the body of pdi function to achieve it. Don't change the signature of the function.

```text
Note -> The online judge can't force you to write the function recursively but that is what the spirit of question is.Write recursive and not iterative logic. The purpose of the question is to aid learning recursion and not test you.

Input Format
A number n

Output Format
n
n - 1
n - 2
..
1
1
2
3
..
n

Constraints
1 <= n <= 1000

Sample Input
3

Sample Output
3
2
1
1
2
3
```
## Dry Run
![Screenshot 2022-01-13 141037](https://user-images.githubusercontent.com/64803628/149295616-acf2537a-63f1-47e5-bae7-d3056820aa3d.png)

## Solution
```java
import java.io.*;
import java.util.*;

public class Main {

      public static void main(String[] args) throws Exception {
        // write your code here
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        printIncreasing(n);
    }

    public static void printIncreasing(int n){
        if(n<=0){
           
            return;
        }
        System.out.println(n);
        printIncreasing(n-1);
        System.out.println(n);
        
        
    }

}
```
