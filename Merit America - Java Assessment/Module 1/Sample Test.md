1. Good URI Design
Which of the following are true regarding good _URI_ design?

Pick **ONE OR MORE** options

□ URIs should never be changed

□ URIs must be constructed by the client

□ URIs should be short in length

□ URIs should be case-sensitive

□ HTTP verbs should be used instead of operation names in URIs

□ Use spaces when designing a URI

□ Redirection must be used if a change in URI is required

---

2. FizzBuzz
Given a nymber _n_, for each integer _i_ in the range from _1_ to _n_ inclusive, print one value per line ad follows:

- if _i_ is a multiple of both 3 and 5, print _FizzBuzz_.
- if _i_ is a multiple of 3 (but not 5), print _Fizz_.
- if _i_ is a multiple of 5 (but not 3), print Buzz.
- if _i_ is not a multiple of 3 or 5, print the value of _i_.

**Function Description**
Complete the function _fizzBuzz_ in the editor below.

fizzBuzz has the following parameter(s):
	_int n_: upper limit of values to test (inclusive)
Returns: NONE
Prints: The function must print the appropriate response for each value _i_ in the set _{1,2, ... n}_ in ascending order, each on a seperate line.

**Constraints**
- _o < n < 2 x 10^5_

**Input Format for Custom Testing**
Input from stdin will be processed as follows and passed to the function.

The single integer _n_, the limit of the range to test: [1, 2, ...n].

**Sample Case 0**

Sample Input:
```shell
STDIN    Function
-----    --------
15    →  n = 15
```

Sample Output:
```shell
1     
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz
```

**Explanation**
The numbers _3, 6, 9, and 12_ are multiples of _3_ (but not 5), so print _Fizz_ on those lines.
The numbers _5 and 10_ are multiples of _5_ (but not 3), so print _Buzz_ on those lines.
The number _15_ is a multiple of both _3_ and _5_, so print _FizzBuzz_ on that line.
None of the other values is a multiple of either _3_ or _5_, so print the value of _i_ on those lines.

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
     * Complete the 'fizzBuzz' function below.
     *
     * The function accepts INTEGER n as parameter.
     */

    public static void fizzBuzz(int n) {

        for (int i = 1; i <= n; i++) {
             if (((i % 5) == 0) && ((i % 3) == 0)) // Is it a multiple of 5 & 3?
                 System.out.println("FizzBuzz");
            else if ((i % 3) == 0) // Is it a multiple of 5?
                 System.out.println("Fizz");
             else if ((i % 5) == 0) // Is it a multiple of 7?
                 System.out.println("Buzz");
            else
                 System.out.println(i); // Not a multiple of 5 or 3
            }

    }

}
public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));

        int n = Integer.parseInt(bufferedReader.readLine().trim());

        Result.fizzBuzz(n);

        bufferedReader.close();
    }
}

```

---

3. Are you an expert on data structures
Which of the following data structures can erase from its beginning or its end in O(1) time?

 Pick **ONE** option

○ Vector

○ deque

○ stack

○ segment tree