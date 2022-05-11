# 1. Double on Match
---
Given an array of long integers '_arr'_ and a number '_num',_ iterate through the elements in _arr_ and double the value of _num_ whenever an element equals _num_. Find the maximum possible value of _num_, knowing that _arr_ can be reordered before the iteration.

**Example**
_arr = [1, 2, 4, 11, 12, 8]_
_num = 2_

Iterating through _arr_:

| arr | num |
| --- | --- |
|     | 2   |
| 1   | 2   |
| 2   | 4   |
| 4   | 8   |
| 11  | 8   |
| 12  | 8   |
| 8   | 16  |

The maximal value of _num = 16._ Note that _arr_ could have been reordered before iterating.

**Function Description**
Complete the function _doubleSize_ in the editor below.

doubleSize has the following parameter(s):
    _long int_ _arr[n]:_  an array of long integers
    _long int_ _num:_ the base long integer

**Returns:**
   _long_ _int:_ the maximal value of _num_

**Constraints**
-   _1 ≤ n ≤ 106_
-   _0 ≤ arr[i] ≤ 1016_
-   _0 ≤ num ≤ 104_

##### Input Format for Custom Testing
Input from stdin will be processed as follows and passed to the function.

The first line contains an integer _n_, the size of the array _arr_.
Each of the next _n_ lines contains an integer _arr[i]_ where _0 ≤ i < n_.
The last line contains a long integer, _num_.

##### Sample Case 0
**Sample Input**
```
STDIN     Function
-----     --------
5    →    arr[] size n = 5
1    →    arr = [1, 2, 3, 1, 2]
2
3
1
2
1    →    num = 1
```

**Sample Output**
```
4
```

**Explanation**
Rearrange _arr_ to _arr = {1, 1, 2, 2, 3}._

| arr | num |
| --- | --- |
|     | 1   |
| 1   | 2   |
| 1   | 2   |
| 2   | 4   |
| 2   | 4   |
| 3   | 4   |
 
##### Sample Case 1
**Sample Input 1**
```
STDIN     Function
-----     --------
3    →    arr[] size n = 3
1    →    arr = [1, 1, 1]
1
1
1    →    num = 1
```

**Sample Output 1**
```
2
```

**Explanation 1**

| arr | num |
| --- | --- |
|     | 1   |
| 1   | 2   |
| 1   | 2   |
| 1   | 2   |

##### Sample Case 2
**Sample Input**
```
STDIN     Function
-----     --------
5    →    arr[] size n = 5
2    →    arr = [2, 5, 4, 6, 8]
5
4
6
8
2    →    num = 2
```

**Sample Output**
```
16
```

**Explanation**

Rearrange _arr_ to _arr = {2, 4, 5, 6, 8}._

| arr | num |
| --- | --- |
|     | 2   |
| 2   | 4   |
| 4   | 8   |
| 5   | 8   |
| 6   | 8   |
| 8   | 16  |

---

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
     * Complete the 'doubleSize' function below.
     *
     * The function is expected to return a LONG_INTEGER.
     * The function accepts following parameters:
     *  1. LONG_INTEGER_ARRAY arr
     *  2. LONG_INTEGER b
     */

    public static long doubleSize(List<Long> arr, long b) {
    // Write your code here

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int arrCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Long> arr = IntStream.range(0, arrCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine().replaceAll("\\s+$", "");
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .map(String::trim)
            .map(Long::parseLong)
            .collect(toList());

        long b = Long.parseLong(bufferedReader.readLine().trim());

        long result = Result.doubleSize(arr, b);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```

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
     * Complete the 'doubleSize' function below.
     *
     * The function is expected to return a LONG_INTEGER.
     * The function accepts following parameters:
     *  1. LONG_INTEGER_ARRAY arr
     *  2. LONG_INTEGER b
     */

    public static long doubleSize(List<Long> arr, long b) {
		Collections.sort(arr);
	        for (long i : arr) {
		        if (i == b) {
	                b = b*2;
            }
        }
	    return b;
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int arrCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Long> arr = IntStream.range(0, arrCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine().replaceAll("\\s+$", "");
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .map(String::trim)
            .map(Long::parseLong)
            .collect(toList());

        long b = Long.parseLong(bufferedReader.readLine().trim());

        long result = Result.doubleSize(arr, b);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```