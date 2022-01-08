# Prime Factorization Of A Number

> 1. You are required to display the prime factorization of a number.
>     2. Take as input a number n.
>     3. Print all its prime factors from smallest to largest.
 ```text                              
Input Format
n, an integer

Output Format
p1  p2  p3  p4.. all prime factors of n

Constraints
2 <= n < 10 ^ 9

Sample Input
1440

Sample Output
2 2 2 2 2 3 3 5

```
## Solution

```java
import java.util.*;

public class Main{

public static void main(String[] args) {
  // write your code here  
  Scanner sc=new Scanner(System.in);
  int n=sc.nextInt();
  for(int i=2;i<n;i++){
     while(n%i==0){
         System.out.print(i+" ");
         n=n/i;
     }
  }
  if(n!=1){
      System.out.print(n);
  }

 }
 
}
```