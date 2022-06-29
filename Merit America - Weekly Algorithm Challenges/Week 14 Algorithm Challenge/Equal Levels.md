# Equal Levels

Two signals are being generated as part of a simulation. A program monitors the signals. Whenever the two signals become equal at the same time, the frequency is noted. A record is maintained for the maximum simultaneous frequency seen so far. Each time a higher simultaneous frequency is noted, this variable (_maxequal)_ is updated to the higher frequency.

Note:
-   Both signals start at time _t=0,_ but their durations might be different. In this case, the comparison of equality is performed only until the end of the shorter signal.
-   If both signals have equal frequencies at a given time but the frequency is less than or equal to the current maximum frequency, _maxequal,_ is not updated.

The running times of both signals are given, denoted by _n_ and _m_ respectively. During the course of the simulation, how many times is the _maxequal_ variable updated?

**Example:**
_signalOne = [1, 2, 3, 3, 3, 5, 4]_
_signalTwo = [1, 2, 3, 4, 3, 5, 4]_ 

![](https://hrcdn.net/s3_pub/istreet-assets/-_2KQZ7eGUdtw5b-eXqoqA/equal_levels_example.svg)

Each of the first three signals match and are increasing, so _maxequal_ is updated _3_ times to _1, 2_ and then _3_.

At the fourth time, they are not equal.

At the fifth, they are equal to _3_. Since _maxequal_ contains _3_ already, it is not updated.

At the sixth time, both signals are equal to _5_. This is greater than _maxequal = 3_, so now _maxequal = 5._

At the final time, signals are equal to _4_. Since _4_ is less than _maxequal_, it is not updated.

_maxEqual_ was updated a total of _4_ times.

**Function Description:**
Complete the _updateTimes_ function in the editor below.

_updateTimes_ has the following parameter(s):
    _int signalOne[n]:_ the frequencies of the first signal
    _int signalTwo[m]:_ the frequencies of the second signal

**Returns:**
    _int:_  the number of updates

**Constraints:**
-   _1 ≤ n ≤ 105_ 
-   _0 ≤ signalOne[i] ≤ 109_
-   _1 ≤ m ≤ 105_
-   _0 ≤ signalTwo[i] ≤ 109_

## Input Format For Custom Testing
The first line contains an integer, _n,_ the running time of the first signal and the number of elements in _signalOne_.

Each line _i_ of the _n_ subsequent lines (where _0 ≤ i < n_) contains the frequency of the _signalOne[i]._

The next line contains an integer, _m,_ the running time of the second signal and the number of elements in _signalTwo_.

Each line _i_ of the _m_ subsequent lines (where 0 ≤ i < m) contains the frequency of the _signalTwo[i]._

## Sample Case 0
**Sample Input 0:**
```
STDIN     Function
-----     --------
5    →    signalOne[] size n = 5
1    →    signalOne = [1, 2, 3, 4, 1]
2
3
4
1
5    →    signalTwo[] size m = 5
5    →    signalTwo = [5, 4, 3, 4, 1]
4
3
4
1
```

**Sample Output 0:**
```
2
```

**Explanation:**
![](https://hrcdn.net/s3_pub/istreet-assets/4GXURla60sdIg3_CN6rQeA/equal_levels_sample_0.svg)

The frequencies are equal during three periods, with frequencies _3, 4_ and _1._

The maximum frequency is updated twice at _3_, and _4_, since _4_ is greater than _3._

It is not updated when their values are _1_ because _1_ is less than the current _maxequal = 4._

## Sample Case 1
**Sample Input 1:**
```
STDIN     Function
-----     --------
5    →    signalOne[] size n = 5
1    →    signalOne = [1, 2, 3, 4, 5]
2
3
4
5
5    →    signalTwo[] size m = 5
5    →    signalTwo = [5, 4, 3, 2, 1]
4
3
2
1
```

**Sample Output 1:**
```
1
```

**Explanation:**
![](https://hrcdn.net/s3_pub/istreet-assets/Lslqu42DPtfALm0Ukk77GA/equal_levels_sample_1.svg)

The maximum frequency is updated once at _3,_ the only point where the signals match.

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
     * Complete the 'updateTimes' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts following parameters:
     *  1. INTEGER_ARRAY signalOne
     *  2. INTEGER_ARRAY signalTwo
     */

    public static int updateTimes(List<Integer> signalOne, List<Integer> signalTwo) {
	// Write your code here
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int signalOneCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> signalOne = IntStream.range(0, signalOneCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine().replaceAll("\\s+$", "");
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .map(String::trim)
            .map(Integer::parseInt)
            .collect(toList());

        int signalTwoCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> signalTwo = IntStream.range(0, signalTwoCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine().replaceAll("\\s+$", "");
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .map(String::trim)
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.updateTimes(signalOne, signalTwo);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```

**Finished Code:**
```java

```