# Compliance Crawler Directory Reset

A compliance crawler utility is used to search out for compliance issues in the file system of any computer starting from the root directory.

A logger logs every time a move operation is performed by the utility. The operations that the utility can perform are given below:
1.  “`../`”: move to the parent folder of the current folder
2.  “`./`”: remain in the same folder
3.  “`x/`”: move to the child folder named _x_

The crawler now has to go back to the root directory as part of a reset operation. Find the minimum steps required to go back to the root directory from the current folder (the folder reached after all the moves have been performed). The logged sequence of operations performed by the utility after entering the root directory is provided.

NOTE: The crawler never tries to go to the parent of the root directory.

***Example:***
_loggedMoves = ['x/', '../', 'y/', 'z/']_

The crawler moves one folder down to folder _x,_ then moves back up to the root directory. Then, the crawler moves down two folders to folder _z._ Two moves are required to get back to the root directory: one move to folder _y_ and another move to the root.

**Function Description:**
Complete the _minimumSteps_ function in the editor below.

_minimumSteps_ has the following parameter(s):
    _loggedMoves[]_: a string array, the moves of the compliance crawler that are logged

**Returns:**
    _int:_ the minimum number of moves

**Constraints:**
-   _1 ≤ n ≤ 10^5_
-   _1 ≤ size of loggedMoves[i] ≤ 10^2_

## Input Format For Custom Testing
The first line contains an integer, _n,_ the number of moves that have been logged.

Each line _i_ of the _n_ subsequent lines (where _0 ≤ i < n_) contains a string that denotes the move that was logged.

## Sample Case 0
**Sample Input 0:**
```
STDIN     Function
-----     -----
5      →  loggedMoves[] size n = 5
x/     →  loggedMoves = ['x/', 'y/', '../', 'z/', './']
y/
../
z/
./
```

**Sample Output 0:**
```
2
```

**Explanation:**
The crawler moves two folders down from the root directory to folder _y_, moves back up one folder, then moves down to another folder _z_. It then performs a move to remain in the same folder. Thus, _2_ moves are required to reach root: one to the parent folder _x_ and then to the root directory.

## Sample Case 1
**Sample Input 1:**
```
STDIN     Function
-----     -----
6      →  loggedMoves[] size n = 6
o/     →  loggedMoves = ['o/', 'w/', 'e/', './', './', './']
w/
e/
./
./
./
```

**Sample Output 1:**
```
3
```

**Explanation:**
The crawler moves three folders down from the root directory to folder _e_. It then performs three moves to remain in the same folder. It takes _3_ moves to reach the root directory.

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
     * Complete the 'minimumSteps' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts STRING_ARRAY loggedMoves as parameter.
     */

    public static int minimumSteps(List<String> loggedMoves) {
	// Write your code here
    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int loggedMovesCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<String> loggedMoves = IntStream.range(0, loggedMovesCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .collect(toList());

        int result = Result.minimumSteps(loggedMoves);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

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
     * Complete the 'minimumSteps' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts STRING_ARRAY loggedMoves as parameter.
     */

    public static int minimumSteps(List<String> loggedMoves) {
        Stack stack = new Stack<>();

        for(String s:loggedMoves) {
            if(s.equals("./")) {
            continue;
        } else if(s.equals("../")) {
            if(!stack.isEmpty()) {
                stack.pop();
            }
        } else {
            stack.push(s);
        }
        }
    return stack.size();
    }
}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int loggedMovesCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<String> loggedMoves = IntStream.range(0, loggedMovesCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine();
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .collect(toList());

        int result = Result.minimumSteps(loggedMoves);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```