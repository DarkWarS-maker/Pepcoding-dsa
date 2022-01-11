# Pattern 16

> 1. You are given a number n.
>       2. You've to write code to print the pattern given in output format below
```text
                                  
Input Format
A number n
Output Format

Constraints
1 <= n <= 10

Sample Input
7

Sample Output
1												1	
1	2										2	1	
1	2	3								3	2	1	
1	2	3	4						4	3	2	1	
1	2	3	4	5				5	4	3	2	1	
1	2	3	4	5	6		6	5	4	3	2	1	
1	2	3	4	5	6	7	6	5	4	3	2	1

```
## Solution

```java
import java.util.*;

public class Main {
  public static void main(String[] args)
  {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    int sp = 2 * n - 3;
    int st = 1;
    for (int i = 1; i <= n; i++)
    {
      int val = 1; //since each row begins with 1
      for (int j = 1; j <= st; j++)
      {
        System.out.print(val + "	");
        val++;
      }
      for (int j = 1; j <= sp; j++)
      {
        System.out.print("	");
      }
      if ( i == n) //Last Row check
      {
        st--; //removing extra star
        val--; //reducing val by 1
      }
      for (int j = 1; j <= st; j++)
      {
        val--; //reducing value first then printing  System.out.print(val + "  ");

      }
      st++;
      sp -= 2;
      System.out.println();
    }
  }
}
```
