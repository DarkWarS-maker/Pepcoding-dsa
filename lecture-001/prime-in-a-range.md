# Print All Primes Till N

> You've to print all prime numbers between a range. 
> Take as input "low", the lower limit of range.
> Take as input "high", the higher limit of range.
> For the range print all the primes numbers between low and high (both included).

```text
Input Format
low 
high

Output Format
n1
n2
.. all primes between low and high (both included)


Constraints
2 <= low < high < 10 ^ 6

Sample Input
6 
24

Sample Output
7
11
13
17
19
23

```
## Dry Run
![Screenshot 2022-01-13 125520](https://user-images.githubusercontent.com/64803628/149284543-0c099fc0-16ec-40fa-8784-2cbce9e5afd1.png)


## Solution

```java
import java.util.*;

public class Main{
    public static void main(String[] args) {
        // write your code here
        Scanner sc=new Scanner(System.in);
        int low=sc.nextInt();
        int high=sc.nextInt();
        for(int j=low;j<=high;j++){
             int n=j;
           boolean flag=true;
           for(int i=2;i*i<=n;i++){
               if(n%i==0){
                   flag=false;
                   break;
               }
           }
           
           if(){
               System.out.println(n);
           }
           else{
               
           }
        }
    }
    
   
}
'''
