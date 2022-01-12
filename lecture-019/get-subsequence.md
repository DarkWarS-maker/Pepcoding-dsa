# Get Subsequence

> 1. You are given a string str.
> 2. Complete the body of getSS function - without changing signature - to calculate all subsequences of str.
Use sample input and output to take idea about subsequences.

> Note -> The online judge can't force you to write the function recursively but that is what the spirit of question is.
> Write recursive and not iterative logic. The purpose of the question is to aid learning recursion and not test you.
```text
Input Format
A string str

Output Format
Contents of the arraylist containing subsequences as shown in sample output

Constraints
0 <= str.length <= 20

Sample Input
abc

Sample Output
[, c, b, bc, a, ac, ab, abc]
```
## Solution
```java
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner sc=new Scanner(System.in);
        String st=sc.nextLine();
        ArrayList<String> ans=gss(st);
        System.out.println(ans);

    }

    public static ArrayList<String> gss(String str) {
        
        if(str.length()==0){
            ArrayList<String> base=new ArrayList<>();
            base.add("");
            return base;
        }
        
        char ch=str.charAt(0);
        ArrayList<String> recAns=gss(str.substring(1));
        ArrayList<String> ans=new ArrayList<>();
        for(String rst:recAns){
            ans.add(rst);
            
            
        }
        for(String rst:recAns){
            ans.add(ch+rst);
        }
        
        return ans;
    }

}
```