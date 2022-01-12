# Get Stair Paths

> 1. You are given a number n representing number of stairs in a staircase.
> 2. You are standing at the bottom of staircase. You are allowed to climb 1 step, 2 steps or 3 steps in one move.
> 3. Complete the body of getStairPaths function - without changing signature - to get the list of all paths that can be used to climb the staircase up.
> Use sample input and output to take idea about output.

```text
Note -> The online judge can't force you to write the function recursively but that is what the spirit of question is. Write recursive and not iterative logic. The purpose of the question is to aid learning recursion and not test you.

Input Format
A number n

Output Format
Contents of the arraylist containing paths as shown in sample output


Constraints
0 <= n <= 10

Sample Input
3

Sample Output
[111, 12, 21, 3]

```
## Solution

```java
import java.io.*;

import java.util.*;

public class Main {

  public static void main(String[] args) throws Exception {
    Scanner scn = new Scanner(System.in);
    int n = scn.nextInt();
    ArrayList< String> paths = getStairPaths(n);
    System.out.println(paths);
  }

  public static ArrayList< String> getStairPaths(int n) {
    if (n == 0) {                                      //1.1
      ArrayList< String> bres = new ArrayList< >();
      bres.add("");
      return bres;
    } 
    else if (n < 0) {
      ArrayList< String> bres = new ArrayList< >();         //1.2
      return bres;
    }

    ArrayList< String> path1 = getStairPaths(n - 1);         //2.1
    ArrayList< String> path2 = getStairPaths(n - 2);         //2.2
    ArrayList< String> path3 = getStairPaths(n - 3);         //2.3

    ArrayList< String> paths = new ArrayList< >();            //3

    for (String path : paths1) {
      paths.add("1" + path);                               //4.1
    }
    for (String path : path2) {
      paths.add("2" + path);                               //4.2
    }
    for (String path : path3) {
      paths.add("3" + path);                               //4.3
    }
    return paths;                                           //5

  }

}
```