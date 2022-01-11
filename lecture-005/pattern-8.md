# Pattern 8

> 1. You are given a number n.
> 2. You've to create a pattern of * and separated by tab as shown in output format.
```text

Input Format
A number n
Output Format


Constraints
1 <= n <= 100
Sample Input
5
Sample Output

				*	
			*		
		*			
	*				
*
```
## Solution
```java
import java.util.*;

public class Main {

    public static void main(String[] args) {
        Scanner scn = new Scanner(System.in);

        // write ur code here
        int n=scn.nextInt();
        int nsp=n-1;
        for(int i=1;i<=n;i++){
            for(int j=1;j<=nsp;j++){
                System.out.print("\t");
            }
            nsp--;
            System.out.println("*\t");
        }

    }
}
```