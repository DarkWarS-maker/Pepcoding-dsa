# Pattern 19

> 1. You are given a number n.
>       2. You've to write code to print the pattern given in output format below
                                  
                                 
                                
                               
                               
```text                               
Input Format
A number n

Output Format

*	*	*		*	
		*		*	
*	*	*	*	*	
*		*			
*		*	*	*	


Constraints
1 <= n <= 10
 Also, n is odd.

Sample Input
3

Sample Output

*	*	*	
*	*	*	
*	*	*	
```
## Solution

```java
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    for (int i = 1 ; i <= n; i++)
    {
      for (int j = 1 ; j <= n; j++)
      {
        if ( i == 1)   {
          if ( j == n || j <= n / 2 + 1)  {
            System.out.print("*	");
          }
          else
          {
            System.out.print("	");
          }
      }
      else if (i <= n / 2)   {
        if ( j == n || j == n / 2 + 1)  {
          System.out.print("*	");
        }
        else
        {
          System.out.print("	");
        }
    }
    else if ( i == n / 2 + 1)   {
      System.out.print("*	");
  }
  else if (i < n)  {
    if (j == 1 || j == n / 2 + 1)  {
      System.out.print("*	");
    }
    else
    {
      System.out.print("	");
    }
}
else //fifth component
{
  if (j == 1 || j >= n / 2 + 1)
  {
    System.out.print("*	");
  }
  else
  {
    System.out.print("	");
  }
}
}
System.out.println();  }
}
}
```