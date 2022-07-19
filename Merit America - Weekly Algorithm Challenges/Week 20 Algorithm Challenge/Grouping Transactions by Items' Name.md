# Grouping Transactions by Items' Names

For a given array of transactions, group all of the transactions by item name. Return an array of strings where each string contains the item name followed by a space and the number of associated transactions.

**Note:** Sort the array descending by transaction count, then ascending alphabetically by item name for items with matching transaction counts.

**Example:**
_transactions = ['notebook', 'notebook', 'mouse', 'keyboard', 'mouse']_

There are two items with _2_ transactions each: _'notebook'_ and _'mouse'._ In alphabetical order, they are _'mouse', 'notebook'._

There is one item with _1_ transaction: '_keyboard'._

The return array, sorted as required, is _['mouse 2', 'notebook 2', 'keyboard 1']._

**Function Description:**
Complete the function _groupTransactions_ in the editor below.

groupTransactions has the following parameter(s):
    _string transactions[n]:_ each _transactions[i]_ denotes the item name in the ith transaction

**Returns:**
    _string[]:_ an array of strings of "item name[space]transaction count" sorted as described

**Constraints:**
-   1 ≤ _n_ ≤ 105
-   1 ≤ length of _transactions[i]_ ≤ 10
-   _transactions[i]_ contains only lowercase English letters, ascii[a-z]

## Input Format Format for Custom Testing
_Input from stdin will be processed as follows and passed to the function._

The first line contains a single integer, _n_, the size of _transactions_.

Each of the next _n_ lines contains a string, the item name for _transactions[i]_.

## Sample Case 0
**Sample Input 0:**
```
STDIN     Function
-----	  -----
4      →  transactions[] size n = 4
bin    →  transactions = ['bin', 'can', 'bin', 'bin']
can
bin
bin
```

**Sample Output 0:**
```
bin 3
can 1
```

**Explanation:**
-   There is one item '_bin_' with _3_ transactions.
-   There is one item '_can_' with _1_ transaction.
-   The return array sorted descending by transaction count, then ascending by name is _['bin 3', 'can 1']._ Sample Case 1Sample Input

## Sample Case 1
**Sample Input 1:**
```
STDIN     Function
-----	  -----
3      →  transactions[] size n = 3
banana →  transactions = ['banana', 'pear', 'apple']
pear
apple
```

**Sample Output 1:**
```
apple 1
banana 1
pear 1
```

**Explanation:**
-   There is one item '_apple_' with _1_ transaction.
-   There is one item _'banana'_ with _1_ transaction.
-   There is one item '_pear_' with _1_ transaction.
-   The return array sorted descending by transaction count, then ascending by name is _['apple 1', 'banana 1', 'pear 1']._

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
     * Complete the 'groupTransactions' function below.
     *
     * The function is expected to return a STRING_ARRAY.
     * The function accepts STRING_ARRAY transactions as parameter.
     */

    public static List<String> groupTransactions(List<String> transactions) {
    // Write your code here
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int transactionsCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<String> transactions = IntStream.range(0, transactionsCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .collect(toList());

        List<String> result = Result.groupTransactions(transactions);

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
     * Complete the 'groupTransactions' function below.
     *
     * The function is expected to return a STRING_ARRAY.
     * The function accepts STRING_ARRAY transactions as parameter.
     */

    public static List<String> groupTransactions(List<String> transactions) {
    // Write your code here
        Map<String, Integer> matches = new TreeMap<>();
       List<String> output = new ArrayList<>();
        int count = 1;
        for(int i = 0; i < transactions.size(); i++){
            if (!matches.containsKey(transactions.get(i))){
                matches.put(transactions.get(i), count);
            } else if (matches.containsKey(transactions.get(i))){
                    matches.put(transactions.get(i), matches.get(transactions.get(i)) + 1);
                }
        }
        for(Map.Entry<String, Integer> item : matches.entrySet()) {
            output.add(item.getKey() + " " + item.getValue());
        }
        return output;
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int transactionsCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<String> transactions = IntStream.range(0, transactionsCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .collect(toList());

        List<String> result = Result.groupTransactions(transactions);

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
