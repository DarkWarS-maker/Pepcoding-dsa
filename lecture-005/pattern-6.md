# Pattern 6

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

*	*	*		*	*	*	
*	*				*	*	
*						*	
*	*				*	*	
*	*	*		*	*	*	

```
## Solution
```java
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);

        // write ur code here
        int n=scn.nextInt();
        int nst=(n/2)+1;
        int nsp=1;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=nst;j++){
                System.out.print("*\t");
            }
            for(int k=1;k<=nsp;k++){
                System.out.print("\t");
            }
            for(int j=1;j<=nst;j++){
                System.out.print("*\t");
            }
            if(i<=n/2){
                nst--;
                nsp+=2;
            }
            else{
                nst++;
                nsp-=2;
            }
            System.out.println();
            
        }

    }
}
```