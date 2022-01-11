# Pattern 20

> 1. You are given a number n.
> 2. You've to write code to print the pattern given in output format below.
```text
Input Format
A number n

Output Format

*				*	
*				*	
*		*		*	
*	*		*	*	
*				*	


Constraints
1 <= n <= 10
 Also, n is odd.

Sample Input
5

Sample Output

*				*	
*				*	
*		*		*	
*	*		*	*	
*				*	
```
## Solution
```java
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    for (int i = 1; i <= n; i++)
    {
      for (int j = 1; j <= n; j++)
      {
        if ( j == 1 || j == n) //if first or last column
        {
          System.out.print("*	");
        }
        else if (i > n / 2 && (i == j || i + j == n + 1)) // part of either
          diagonal below middle row
        {
          System.out.print("*	");
        }
        else
        {
          System.out.print("	");
        }
      }
      System.out.println();
    }
  }
}
```