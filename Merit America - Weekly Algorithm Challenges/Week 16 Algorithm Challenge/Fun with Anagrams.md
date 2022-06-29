# Fun with Anagrams

Two strings are anagrams if they are permutations of each other. In other words, both strings have the same size and the same characters. For example, "aaagmnrs" is an anagram of "anagrams". Given an array of strings, remove each string that is an anagram of an earlier string, then return the remaining array in sorted order.

**Example:**
_str = ['code', 'doce', 'ecod', 'framer', 'frame']_

-   "_code"_ and "_doce"_ are anagrams. Remove "doce" from the array and keep the first occurrence _"code"_ in the array.
-   _"code"_ and "_ecod"_ are anagrams. Remove "ecod" from the array and keep the first occurrence _"code"_ in the array.
-   _"code"_ and "_framer"_ are not anagrams_._ Keep both strings in the array.
-   "_framer"_ and "_frame"_ are not anagrams due to the extra _'r'_ in _'framer'._ Keep both strings in the array.
-   Order the remaining strings in ascending order: _[ "code","frame","framer"]_.

 

**Function Description:**
Complete the function _funWithAnagrams_ in the editor below.

_funWithAnagrams_ has the following parameters:
    _string text[n]:_  an array of strings

**Returns:**
    _string[m]:_  an array of the remaining strings in ascending alphabetical order,.

**Constraints:**
-    _0 ≤ n ≤ 1000_
-   _0 ≤ m ≤ n_
-   _1 ≤_ length of _text[i] ≤ 1000_
-   Each string _text[i]_ is made up of characters in the range ascii[a-z].

## Input Format For Custom Testing
The first line contains an integer, _n_, that denotes the number of elements in _text_.  
Each line _i_ of the _n_ subsequent lines (where _0 ≤ i < n_) contains a string that describes _text[i]_.

## Sample Case 0
**Sample Input 0:**
```
STDIN       Function 
-----       -------- 
4        →  n = 4
code     →  text = ["code","aaagmnrs","anagrams","doce"] 
aaagmnrs
anagrams
doce
```

**Sample Output 0:**
```
aaagmnrs
code
```

**Explanation:**
-   "_code"_ and "_doce"_ are anagrams. Remove "_doce_" and keep the first occurrence _"code"_ in the array.
-   _"aaagmnrs"_ and "_anagrams"_ are anagrams. Remove "a_nagrams_" and keep the first occurrence _"aaagmnrs"_ in the array.
-   Order the remaining strings in ascending order:  _["aaagmnrs", "code"]._

## Sample Case 1
**Sample Input 1:**
```
STDIN     Function
-----     --------
4      →  n = 4
poke   →  text = ["poke","pkoe","okpe","ekop"]
pkoe
okpe
ekop
```

**Sample Output 1:**
```
poke
```

**Explanation:**
-   _"poke_" and _"pkoe"_ are anagrams. Remove _"pkoe"_ and keep the first occurrence _"poke"_  in the array.
-   _"poke"_ and _"okpe"_ are anagrams. Remove _"okpe"_ and keep the first occurrence _"poke"_ in the array.
-   _"poke"_  and _"ekop"_ are anagrams. Remove _"ekop"_ and keep the first occurrence _"poke"_ in the array.
-   Order the remaining strings in ascending order: _["poke"]_.

---

**Starter Code:**
```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;



class Result {

    /*
     * Complete the 'funWithAnagrams' function below.
     *
     * The function is expected to return a STRING_ARRAY.
     * The function accepts STRING_ARRAY text as parameter.
     */

    public static List<String> funWithAnagrams(List<String> text) {
	//Write your code here
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int textCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<String> text = IntStream.range(0, textCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .collect(toList());

        List<String> result = Result.funWithAnagrams(text);

        bufferedWriter.write(
            result.stream()
                .collect(joining("\n"))
            + "\n"
        );

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```

**Finished Code:**
```java
import java.io.*;
import java.math.*;
import java.security.*;
import java.text.*;
import java.util.*;
import java.util.concurrent.*;
import java.util.function.*;
import java.util.regex.*;
import java.util.stream.*;
import static java.util.stream.Collectors.joining;
import static java.util.stream.Collectors.toList;



class Result {

    /*
     * Complete the 'funWithAnagrams' function below.
     *
     * The function is expected to return a STRING_ARRAY.
     * The function accepts STRING_ARRAY text as parameter.
     */

    public static List<String> funWithAnagrams(List<String> text) {
        List<String> newText = new ArrayList<>();
        Collection<String> temp = new HashSet<>();
        for (String str : text){
            char []first = str.toCharArray();
            Arrays.sort(first);
            
            if(!temp.contains(new String(first))){
                newText.add(str);
                temp.add(new String(first));
            }
            System.out.println(first);
        }
        Collections.sort(newText);
        return newText;
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int textCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<String> text = IntStream.range(0, textCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .collect(toList());

        List<String> result = Result.funWithAnagrams(text);

        bufferedWriter.write(
            result.stream()
                .collect(joining("\n"))
            + "\n"
        );

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```