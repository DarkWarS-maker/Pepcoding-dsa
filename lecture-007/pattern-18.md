# Pattern 18

> 1. You are given a number n.
>       2. You've to write code to print the pattern given in output format below
                               
                               
```text                              
Input Format
A number n

Output Format


TConstraints
1 <= n <= 10
 Also, n is odd.

Sample Input
7
Sample Output

*	*	*	*	*	*	*	
	*				*	
		*		*	
			*	
		*	*	*	
	*	*	*	*	*	
*	*	*	*	*	*	*	
```
## Solution
```java
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int sp = 0; // there are 0 spaces in first row
    int st = n; // there are n stars in first row
    for (int i = 1; i <= n; i++)
    {
      for (int j = 1; j <= sp; j++) // for printing spaces
      {
        System.out.print("	");

      }
      for (int j = 1; j <= st; j++)
      {
        if ( i > 1 && i <= n / 2 && j > 1 && j < st) //if the row is between middl e row and first row
        { //if the star is not the firs t or last of the row
          System.out.print("	");
        }
        else
        {
          System.out.print("*	");
        }
      }
      if ( i <= n / 2)
      {
        st -= 2;
        sp++;
      }
      else
      {
        st += 2;
        sp--;
      }
      System.out.println();
    }
  }
}
```