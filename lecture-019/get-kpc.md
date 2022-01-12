# Get Kpc

> 1. You are given a string str. The string str will contains numbers only, where each number stands for a key pressed on a mobile phone.
> 2. The following list is the key to characters map :
    0 -> .;
    1 -> abc
    2 -> def
    3 -> ghi
    4 -> jkl
    5 -> mno
    6 -> pqrs
    7 -> tu
    8 -> vwx
    9 -> yz
> 3. Complete the body of getKPC function - without changing signature - to get the list of all words that could be produced by the keys in str.
> Use sample input and output to take idea about output.

> Note -> The online judge can't force you to write the function recursively but that is what the spirit of question is. Write recursive and not iterative logic. The purpose of the question is to aid learning recursion and not test you.

```text
Input Format
A string str

Output Format
Contents of the arraylist containing words as shown in sample output

Constraints
0 <= str.length <= 10
str contains numbers only

Sample Input
78

Sample Output
[tv, tw, tx, uv, uw, ux]

```
## Solution
```java
import java.io.*;
import java.util.*;

public class Main {

    public static void main(String[] args) throws Exception {
        Scanner sc=new Scanner(System.in);
        String str=sc.nextLine();
        ArrayList<String> ans=getKPC(str);
        System.out.println(ans);

    }
    static String[] codes = {".;", "abc", "def", "ghi", "jkl", "mno", "pqrs", "tu", "vwx",
                           "yz"
                          }; 

    public static ArrayList<String> getKPC(String str) {
        if(str.length()==0){
            ArrayList<String> bs=new ArrayList<>();
            bs.add("");
            return bs;
        }
        char ch=str.charAt(0);
        String mycode=codes[ch-'0'];
        ArrayList<String> recAns=getKPC(str.substring(1));
        ArrayList<String> myAns=new ArrayList<>();
        for(int i=0;i<mycode.length();i++){
            char ch1=mycode.charAt(i);
            for(String st:recAns){
                myAns.add(ch1+st);
            }
        }
        return myAns;
        
    }

}
```