# Digits Of A Number

> 1. You've to display the digits of a number.
> 2. Take as input "n", the number for which digits have to be displayed.
> 3. Print the digits of the number line-wise.

```text
Input Format
"n" where n is any integer.
Output Format
d1
d2
d3
... digits of the number

Constraints
1 <= n < 10^9

Sample Input
65784383

Sample Output
6
5
7
8
4
3
8
3

```
## Solution

```java
import java.util.*;
    
    public class Main{
    
    public static void main(String[] args) {
       
      Scanner sc=new Scanner(System.in);
      int n=sc.nextInt();
      int temp=n;
      int div=1;
      while(temp>10){
          temp=temp/10;
          div*=10;
      }
      while(div!=0){
          int digit=n/div;
          System.out.println(digit);
          n=n%div;
          div=div/10;
      }
     }
  
    }
```