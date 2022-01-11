# Pattern 11

> 1. You are given a number n.
> 2. You've to create a pattern as shown in output format.
```text
Input Format
A number n
Output Format

Constraints
1 <= n <= 44
Sample Input
5
Sample Output
1	
2	3	
4	5	6	
7	8	9	10	
11	12	13	14	15
```
## Solution
```
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int val = 1; //initializing value variable
    for (int i = 1; i <= n; i++)
    {
      for (int j = 1; j <= i; j++)
      {
        System.out.print( val + "	"); // printing val + space  val++; // incrementing val by 1  }
        System.out.println();
      }
    }
  }
  
```