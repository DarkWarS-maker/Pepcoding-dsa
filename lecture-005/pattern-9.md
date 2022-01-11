# Pattern 9

> 1. You are given a number n.
> 2. You've to create a pattern of * and separated by tab as shown in output format.
```text
Input Format
A number n
Output Format

Constraints
1 <= n <= 100
 Also, n is odd.

Sample Input
5

Sample Output

*				*	
	*		*		
		*			
	*		*		
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
    for (int i = 1; i <= n; i++) //decides the number of rows for output printing  {
      for (int j = 1; j <= n; j++) //prints the stars in the row
      {
        if (i == j || i + j == n + 1)
        {
          System.out.print("*	");
        }
        else
          System.out.print("	");
      }
    System.out.println(); //changes the row on output console  }
  }
}
```