# Pattern 15

> 1. You are given a number n.
> 2. You've to write code to print the pattern given in output format below.
```text

Input Format
A number n

Output Format

Constraints
1 <= n <= 10
 Also, n is odd.

Sample Input
5

Sample Output
		1	
	2	3	2	
3	4	5	4	3	
	2	3	2	
		1	
```
## Solution
```java
import java.util.*;

public class Main {
  public static void main(String[] args)  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int sp = n / 2;
    int st = 1;
    int val = 1; //intializing val  for(int i = 1; i<= n;i++)
    {
      for (int j = 1; j <= sp; j++)  {
        System.out.print("	");
      }
      for (int j = 1; j <= st; j++)  {
        System.out.print(val + "	");
      }
      if (i <= n / 2)
      {
        sp--;
        st += 2;
      }
      else
      {
        sp++;
        st -= 2;
      }
      val++; //increasing val by 1  System.out.println();
    }
  }
}
```