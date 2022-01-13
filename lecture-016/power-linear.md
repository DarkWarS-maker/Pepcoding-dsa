# Power-linear

> 1. You are given a number x.
> 2. You are given another number n.
> 3. You are required to calculate x raised to the power n. Don't change the signature of power function .

```text
Note -> The online judge can't force you to write the function recursively but that is what the spirit of question is. Write recursive and not iterative logic. The purpose of the question is to aid learning recursion and not test you.

Input Format
A number x
A number n

Output Format
x raised to the power n

Constraints
1 <= x <= 10
0 <= n <= 9

Sample Input
2
5

Sample Output
32
```
## Dry Run
![Screenshot 2022-01-13 141453](https://user-images.githubusercontent.com/64803628/149296291-f6465839-a22f-49a1-8d7e-aeb254783392.png)

## Solution
```java
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        // write your code here
        Scanner sc=new Scanner(System.in);
        int x=sc.nextInt();
        int n=sc.nextInt();
        int ans=power(x,n);
        System.out.println(ans);
    }

    public static int power(int x, int n){
        if(n==0){
            return 1;
        }
        int recAns=power(x,n-1);
        
        return recAns*x;
    }

}
```
