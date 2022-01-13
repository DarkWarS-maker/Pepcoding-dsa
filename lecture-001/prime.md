# Is A Number Prime

> You've to check whether a given number is prime or not.
> Take a number "t" as input representing count of input numbers to be tested.
> Take a number "n" as input "t" number of times.
> For each input value of n, print "prime" if the number is prime and "not prime" otherwise.

```text

Input Format
A number t
A number n
A number n
.. t number of times

Output Format
prime
not prime
not prime
.. t number of times

Constraints
1 <= t <= 10000
2 <= n < 10^9
Sample Input
5
13
2
3
4
5
Sample Output
prime
prime
prime
not prime
prime

```
## Dry Run
![Screenshot 2022-01-13 124744](https://user-images.githubusercontent.com/64803628/149283566-fb74186a-4fd6-43f1-8539-b46e5e76b09d.png)

## Solution

```java
import java.util.*;

  public class Main{

 public static boolean checkPrime(int n){

     for(int i=2;i*i<=n;i++){
               if(n%i==0){

                   return false;

               }
           }
           return true;

 }

  public static void main(String[] args) {
      Scanner scn = new Scanner(System.in);
       int t=scn.nextInt();
       while(t>0){
           int n=scn.nextInt();
           boolean isprime=checkPrime(n);;

           if(isprime){
               System.out.println("prime");
           }
           else{
               System.out.println("not prime");
           }
           t--;

       }
   }
}
```
