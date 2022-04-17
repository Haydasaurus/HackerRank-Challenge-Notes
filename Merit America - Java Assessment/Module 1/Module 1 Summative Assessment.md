### 1. Java: `Abstract` Classes
Which of the following is true about Java abstract classes?

Pick **ONE** option

◉ An abstract class can extend from a concrete class or form an abstract class.

○ An abstract class can only have abstract methods.

○ A class can extend multiple abstract classes.

○ An abstract class cannot have variables declared inside the class.

---

### 2. Checked Versus Unchecked Exceptions
Which of the following statements are **true** about checked and unchecked exceptions?

Pick **ONE OR MORE** options

■ `NullPointerException` is an example of unchecked exception

■ Checked exception is required to be handled at compile time.

□ `ClassNotFoundException` is an example of unchecked exception.

□ Both of these exceptions can be handled using try, catch and finally keywords.

---

### 3. The `Map` Interface
The `map` interface is implemented by which of the following classes:

Pick **ONE OR MORE** options

■ `HashMap`

□ `DynamicList`

□ `Stack`

■ `TreeMap`

---

### 4. Which of the following is **not** a correct way of commenting?

Pick **ONE** option

○ `/* Here is a comment **** */`

◉ `/* This is also a comment /* More comments */*/`

○ `/ This is also a comment // More comments */`

○ `// /* This is a // // comment */`

---

### 5. Java : OOPS
What feature allows different metods to have the same name and arguments type, but a different implementation is called?

Pick **ONE** option

◉ overloading

○ overriding

○ Java does not permit methods with the same name and type signature

○ None of the above

---

### 6. Abstract Classes
Which of the following is true about abstract classes in Java?

Pick **ONE OR MORE** options

■ abstract classes can be used as just any other class

■ abstract classes need to be declared with `abstract` keyword

■ abstract classes cannot be instantiated

□ a class containing at least one abstract method will be an abstract class

---

### 7. Type Promotions
Given the following type declarations:
```java
int a;
double b;
float c;
long d;
```

The expression _(a + d) * (c + b)_ will be promoted to which of the following?

○ `long`

◉ `double`

○ `int`

○ `float`

---

### 8. Which of the following data types in Java are primitive?

Pick **ONE OR MORE** options

□ `String`

□ `Struct`

■ `Boolean`

■ `char`

---

### 9. Classes Extend Classes
Consider the following three classes:
```java
class A {}
class B extends A {}
class C extends B {}
```

Consider an object of class B is instantiated, i.e.,
```java
B b = new B();
```

Which of the following  boolean expressions evaluates to **true**:

Pick **ONE OR MORE** options

□ `(b instanceof B)`

□ `(b instanceof B) && (!(b instanceof A))`

■ `(b instanceof B) && (!(b instanceof C))`

□ None of the above

---

### 10.  What will be the output of the program?

```java
public class X {

	public static void main(String [] args) {
		
		try {
			badMethod();
			System.out.print("A");
		}

		catch (Exception ex) {
			System.out.print("B");
		} 

		finally {
			System.out.print("C");
		}

		System.out.print("D");
	}

	public static void badMethod() {
		throw new RuntimeException();
	}
	
}
```

Pick **ONE** option

○ AB

○ BC

○ ABC

◉ BCD

---

### 11. Static Code Analysis 9
What will be the output?

```java
class Exc0 extends Exception {}
class Exc1 extends Exc0 {}                         /* Line 2 */
public class Test {

	public static void main(String args[]) {
	
		try {
			throw new Exc1();                      /* Line 9 */
		}

		catch (Exc0 e0) {                          /* Line 11 */
			System.out.println("Ex0 caught");
		}

		catch (Exception e) {
			System.out.println("exception caught");
		}
	}
}
```

Pick **ONE** option

○ Exception caught

◉ Ex0 caught

○ Compilation fails because of an error at line 2.

○ Compilation fails because of an error at line 2.

---

### 12. Which of the following is TRUE?

Pick **ONE** option

◉ In Java, an instance field declared public generates a compilation error.

○ int is the name of a class available in the package java.lang

○ Instance variable names may only contain letters and digits.

○ A class has always a constructor (possibly automatically supplied by the java compiler)

---

### 13. Field Names in Classes
A public data member with the same name is provided in both base as well as derived classes. Which of the following is true?

Pick **ONE** option

○ It is a compiler error to provide a field with the same name in both base and derived class

○ The program will compile and this feature is called overloading

◉ The program will compile and this feature is called overriding

○ The program will compile and this feature is called 'hiding' or 'shadowing'

---

### 14. Java Data Types
`int`, `double`, `Float` are all examples of primitive data types in Java.

True or False?

Pick **ONE** option

◉ False

○ True

---

### 15. Which of the following statements is true?

```java
public void foo( boolean a, boolean b) {

	if( a ) {
		System.out.println("A");
	}

	else if(a && b) {
		System.out.println( "A && B");
	}

	else {
	
		if ( !b ) {
			System.out.println( "notB" );
		}

		else {
			System.out.println( "ELSE" );
		}
	
	}

}
```

Pick **ONE** option

○ If a is true and b is true then the output is "A && B"

○ If a is true and b is false then the output is "notB"

◉ If a is false and b is true then the output is "ELSE"

○ If a is false and b is false then the output is "ELSE"

---

### 16. Value of k After Function Runs
Which is true of the following program?
```java
public class TestFirstApp {
	static void doIt(int x, int y, int m) {
		if (x == 5) {
			m=y;
		} else {
			m=x;
		}
	}	
}

public static void main(String[] args) {
	int i=6, j=4, k=9;
	TestFirstApp.doIt(i,j,k);
	System.out.print(k);
}
```

Pick **ONE** option

○ Doesn't matter what the values of i and j are, the output will always be 5.

○ Doesn't matter what the values of k and j are, the output will always be 5.

◉ Doesn't matter what the values of i and j are, the output will always be 9.

○ Doesn't matter what the values of k and j are, the output will always be 9.

---

### 17. Compiler Output
The Java compiler generates code in

Pick **ONE** option

○ assembly language

○ machine code

○ p-code

◉ byte code

---

### 18. Java: Constructor, Exception Handling and Inheritance
What should be the output of the following code?
```java
class AirPlane {
	public AirPlane() throws IOException {
		System.out.print("AirPlane");
		throw new IOException();
	}
}

class AirJet extends AirPlane {
	Public AirJet() throws IOException{
		System.out.println("AirJet");
		try {
			super();
		} catch (IOExcepton e) {
			System.out.print("IOException is thrown in AirJet");
		}
	}
}

public class Tester {
	public static void main(String[] args) {
		try {
			new AirJet();
		} catch (IOException e) {
			System.out.print("IOException is thrown in Tester");
		}
	}
}
```

Pick **ONE** option

○ "AirPlaneIOException is thrown in AirJet" will be printed.

○ "AirPlaneIOException is thrown in AirJetIOException" will be printed.

○ "AirPlaneIOException is thrown in Tester" will be printed.

◉ The code does not compile because of an error in the constructor class AirJet

---

### 19. Java Print a Sum
What is the output of the following code?
```java
1. public class A {
2.      int add(int i, int j) {
3.           return i+j;
4.      }
5. }
6. public class B extends A {
7.      public static void main(String argv[]) {
8.           short s = 9;
9.           System.out.println(add(s,6));
10.      }
11. }
```

Pick **ONE** option

◉ Compilation fails due to an error on line 2

○ Compilation fails due to an error on line 9, non-static method reference from a static context.

○ Compilation fails due to a type mismatch on line 9.

○ 15

---

### 20. Arrays in Java
Which of the following statements are true?

Pick **ONE** option

◉ Arrays in Java are essentially objects.

○ it is not possible to assign one array to another. Inividual elements of array can however be assigned.

○ Array elements are indexed from 1 to size of array.

○ If a method tries to access an array element beyond its range, a compile warning is generated.

---

### 21. What is the result of compiling and running the fllowing program?
```java
class test {
	public static void main(String args[]) {
		int[] arr = {1,2,3,4};
		call_array(arr[0], arr);
		System.out.println(arr[0] + "," + arr[1]);
	}
	static void call_array(int 1, int arr[]) {
		arr[i] = 6;
		i = 5;
	}
}
```

○ 1,2

○ 5,2

◉ 1,6

○ 5,6

---

### 22. Which of the following statements is correct? Select the one correct answer.

Pick **ONE** option

○ Each Java file must have exactly one package statement to specify where the class is stored.

○ If a Java file has both an import and a package statement, the import statement must come before package statement.

○ A Java file must have at least one class defined. 

◉ If a Java file has a package statement, it must be the first statement (except comments).

---

### 23. Java Execution Flow
What is the result of the following program?
```java
public class Test {
	public static void main(String args []) {
		boolean a = false;
		if (a = true)
			System.out.println("Hello");
		else	
			System.out.println("Goodbye");
	}
}
```

Pick **ONE** option

○ Program produces no putput but terminates correctly.

○ Program does not terminate.

◉ Prints out "Hello"

○ Prints out "Goodbye"

---

### 24.Calling a Constructor
Where in a constructor, can you place a call to a constructor defined in the super class?

Pick **ONE** option

○ Anywhere

◉ The first statement in the constructor

○ The last statement in the constructor

○ You can't call super in a constructor

---

### 25. Which of the following statements is correct?
which of the following statements is correct for a method which is overriding the following method:
```java
public void add(int a) {...}
```

◉ the overriding method must return void

○ the overriding method must return `int`

○ the overriding method can return whatever it likes

---

### 26. Java: String Array
Which of the following Java declaration of the String array is correct?

Pick **ONE** option

◉ String temp [] = new String {"j" "a" "z"};

○ String temp [] = {"j" "b" "c"};

○ String temp = {"a", "b", "c"};

○ String temp [] = {"a", "b", "c"};

---

### 27. Which of he following will output -4.0?

Pick **ONE** option

○ System.out.println(Math.floor(-4.7));

○ System.out.println(Math.round(-4.7));

◉ System.out.println(Math.ceil(-4.7));

○ System.out.println(Math.Min(-4.7));

---

### 28. "Syntax Review 2"
What is the result of trying to compile and run this program?
```java
public class Test {
	public static void main(String[] args) {
		int[] a = {1};
		Test t = new Test();
		t.increment(a);
		System.out.println(a[a.length - 1]);
	}
	void increment(int[] i){
		i[i.length - 1]++;
	}
}
```

Pick **ONE** option

○ It generates a compiler error.

◉ It compiles and prints 2.

○ It compiles and prints 1.

○ It compiles and generates an ArrayIndexOutOfBounds exception at runtime.

---

### 29. Java String Concatenation
What is the output of the following program?
```java
public class Question {
	public static void main(String args[]) {
		String s1 = "abc";
		String s2 = "def";
		String s3 = s1.concat(s2.toUpperCase( ) );
		System.out.println(s1+s2+s3);
	}
}
```

Pick **ONE** option

○ abcdefabcdef

○ abcabcDEFDEF

◉ abcdefabcDEF

○ None of the above

---

### 30. Declarations
Given the following declarations
```java
String s1=new String("Hello")
String s1=new String("there");
String s1=new String();
```
which of the following are legal operations?

Pick **ONE** option

◉ s3=s1 + s2;

○ s3=s1 - s2;

○ s3=s1 & s2

○ s3=s1 && s2

---

### 31. "Syntax Review 1"
The following code is in a file called Test.java
```java
class Base {
	public static void main(String[] args) {
	System.out.println("Hello");
	}
}
public class Test extends Base{}
```
What happens when it is compiled and run?

○ It fails to compile.

○ It compiles and generates a runtime error.

○ It compiles and runs with no output.

◉ It compiles and prints "Hello".

---

### 32. Sum Them All
Calculate the sum of an array of integers.

**Example**
_numbers = [3, 13, 4, 11, 9]_

The sum is _3 + 13 + 4 + 11 + 9_ = _40._

**Function Description**
Complete the function _arraySum_ in the editor below.

arraySum has the following parameter(s):
    _int numbers [n]]:_ an array of integers

**Returns**
    _int:_ integer sum of the numbers array

**Constraints**
-   _1 ≤ n ≤ 104_
-   _1 ≤ numbers[i] ≤ 104_

##### Input Format for Custom Testing
Input from stdin will be processed as follows and passed to the function.

The first line contains an integer _n_, the size of the array _numbers_.

Each of the next _n_ lines contains an integer _numbers[i]_ where _0 ≤ i < n_.

##### Sample Case 0
**Sample Input 0**
STDIN      Function
-----      --------
5      →   numbers[] size n = 5
1      →   numbers = [1, 2, 3, 4, 5]
2
3
4
5

**Sample Output 0**
15

**Explanation 0**
_1 + 2 + 3 + 4 + 5 = 15_.

##### Sample Case 1
**Sample Input 1**
STDIN      Function
-----      --------
2      →   numbers[] size n = 2
12     →   numbers = [12, 12]
12

**Sample Output 1**
24

**Explanation 1**
_12 + 12 = 24_.

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
     * Complete the 'arraySum' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts INTEGER_ARRAY numbers as parameter.
     */

    public static int arraySum(List<Integer> numbers) {
    // Write your code here
       
        int sum = 0;
        for (int i: numbers) {
            sum += i;
        }
        return sum;       
    }                

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        int numbersCount = Integer.parseInt(bufferedReader.readLine().trim());

        List<Integer> numbers = IntStream.range(0, numbersCount).mapToObj(i -> {
            try {
                return bufferedReader.readLine().replaceAll("\\s+$", "");
            } catch (IOException ex) {
                throw new RuntimeException(ex);
            }
        })
            .map(String::trim)
            .map(Integer::parseInt)
            .collect(toList());

        int result = Result.arraySum(numbers);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}

```

---

### 33. The Adder Class
There are different kinds of calculators which are available in the market for different purposes. Sam wants to make a calculator which can return the sum of two integers.

Implement the `Adder` class which should follow the following:

-   It should inherit from the `Calculator` class .
-   It should implement the method `add(int a, int b)` which should calculate and return the sum of two integer parameters, _a_ and _b._

The locked stub code in the editor consists of the following:

-   An abstract class named `Calculator` which contains an abstract method, `add(int a, int b)`.
-   A solution class which
    -   creates an object of the `Adder` class. 
    -   reads the inputs and passes them in a method called by the object of the `Adder` class.

**Constraints**
-   _0 < a, b <_ _105_

##### Input Format For Custom Testing
The only line contains two space-separated integers, _a_ and _b._

##### Sample Case 0
**Sample Input For Custom Testing**
1 1

**Sample Output**
The sum is: 2

**Explanation**
When the _add_ method is called with the arguments _a = 1_ and _b = 1_, it calculates and returns their sum as _1 + 1 = 2_, which is then printed.

##### Sample Case 1
**Sample Input For Custom Testing**
2 3

**Sample Output**
5

**Explanation**
When the _add_ method is called with the arguments _a = 2_ and _b = 3_, it calculates and returns their sum as 2 _+ 3 = 5_, which is then printed.


```java
import java.util.Scanner;

abstract class Calculator {
    abstract int add(int a, int b);
}

/*
 Write the Adder class here. Do not use an access modifier at the beginning of your class declaration.
 */
 
class Adder extends Calculator{
    int add(int a, int b) {
        return a+b;
    }    
}

public class Solution {
    public static void main(String[] args) {
        int a, b;
        try (Scanner scan = new Scanner(System.in)) {
            a = scan.nextInt();
            b = scan.nextInt();
        }

        Calculator adderObject = new Adder();
        System.out.println("The sum is: " + adderObject.add(a, b));
    }
}
```

---

### 34. Balancing Parentheses
Given a string that consists of left and right parentheses, `'('` and `')'`, balance the parentheses by inserting parentheses as necessary. Determine the minimum number of characters that must be inserted.  

**Example**
_s = '(()))'_

Insert _1_ left parenthesis at the left end of the string to get '((()))'. The string is balanced after _1_ insertion.

**Constraints**
-   1 ≤ length of _s_ ≤ 105
    

##### Input Format For Custom Testing
The first line contains a string, _s_, the initial parentheses sequence.

##### Sample Case 0
**Sample Input**

STDIN     Function
-----     -----
()))   →  s = '()))'

**Sample Output**
2

**Explanation**
Insert a '(' _2_ times at the beginning of the string to make it valid: '((()))'.

##### Sample Case 1
**Sample Input**
STDIN     Function
-----     -----
()()   →  s = '()()'

**Sample Output**
0

**Explanation**
The sequence is already valid, so no insertions are needed.

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
     * Complete the 'getMin' function below.
     *
     * The function is expected to return an INTEGER.
     * The function accepts STRING s as parameter.
     */

    public static int getMin(String s) {
    // Write your code here

        int left = 0;
        int right = 0;
        
        for (int i = 0; i < s.length(); ++i) {
            left += s.charAt(i) == '(' ? 1 : -1;
    
            if (left == -1) {
                right += 1;
                left += 1;
            }
        }
       
        return left + right;

    }

}

public class Solution {
    public static void main(String[] args) throws IOException {
        BufferedReader bufferedReader = new BufferedReader(new InputStreamReader(System.in));
        BufferedWriter bufferedWriter = new BufferedWriter(new FileWriter(System.getenv("OUTPUT_PATH")));

        String s = bufferedReader.readLine();

        int result = Result.getMin(s);

        bufferedWriter.write(String.valueOf(result));
        bufferedWriter.newLine();

        bufferedReader.close();
        bufferedWriter.close();
    }
}
```