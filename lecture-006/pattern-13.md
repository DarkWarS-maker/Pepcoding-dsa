# Pattern 13

> 1. You are given a number n.
> 2. You've to create a pattern as shown in output format
```text                               
Input Format
A number n

Output Format

Constraints
1 <= n <= 10

Sample Input
5

Sample Output
1	
1	1	
1	2	1	
1	3	3	1	
1	4	6	4	1	
```
## Solution
```java
import java.util.*;

public class Main {
  public static void main(String[] args)  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    for (int i = 0; i < n; i++ )
    {
      int icj = 1;
      for (int j = 0; j <= i; j++)  {
        System.out.print( icj + "	");
        int icjp1 = (icj * (i - j)) / (j + 1);
        icj = icjp1;

      }
      System.out.println();
    }
  }
}
```