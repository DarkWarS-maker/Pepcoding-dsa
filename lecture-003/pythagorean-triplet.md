# Pythagorean Triplet

> 1. You are required to check if a given set of numbers is a valid pythagorean triplet.
> 2. Take as input three numbers a, b and c.
> 3. Print true if they can form a pythagorean triplet and false otherwise.
```text
Input Format
a, an integer
b, an integer
c, an integer

Output Format
true if the numbers form a pythagorean triplet and false otherwise

Constraints
1 <= a <= 10^9
1 <= b <= 10^9
1 <= c <= 10^9

Sample Input
5 3 4

Sample Output
true
```
## Solution

```java
import java.util.*;
  
  public class Main{
  
  public static void main(String[] args) {
    // write your code here 
    Scanner sc=new Scanner(System.in);
    int a=sc.nextInt();
    int b=sc.nextInt();
    int c=sc.nextInt();
    int max=a;
    if(max<b){
        max=b;
    }
    else if(max<c){
        max=c;
    }
    if(max==a && a*a==b*b+c*c){
        System.out.println(true);
    }
    else if(max==b && b*b==a*a+c*c){
        System.out.println(true);
    }
    else if(max==c && c*c==b*b+a*a){
        System.out.println(true);
    }
    else{
        System.out.println(false);
    }
   }
  }
```