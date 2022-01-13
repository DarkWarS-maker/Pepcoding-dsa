# Factorial

> 1. You are given a number n.
> 2. You are required to calculate the factorial of the number. Don't change the signature of factorial function.

```text
Note -> The online judge can't force you to write the function recursively but that is what the spirit of question is.Write recursive and not iterative logic. The purpose of the question is to aid learning recursion and not test you.

Input Format
A number n

Output Format
factorial of n

Constraints
0 <= n <= 10

Sample Input
5

Sample Output
120
```
## Dry Run
![Screenshot 2022-01-13 141811](https://user-images.githubusercontent.com/64803628/149296722-2e5f2014-cb9b-4fd1-b7d2-edb2ba526b77.png)

## Solution
```java
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        // write your code here
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
       int ans= factorial(n);
       System.out.print(ans);
    }

    public static int factorial(int n){
        
        if(n==0){
            return 1;
        }
        
        int recAns=factorial(n-1);
        
        return recAns*n;
    }

}
```
