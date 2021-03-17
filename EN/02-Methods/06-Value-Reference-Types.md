# Value and Reference Types

[slide hideTitle]

# Value Types

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/03.Java-Fundamentals-Methods/EN/interactive-java-fundamentals-methods-38-Value-types-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

A variable of a **value** \(primitive data\) type contains an instance of the type and holds its value directly. 

Primitive data types (or value types) contain the value of a variable inside their own memory location.

With value types, each variable has **its own copy of the data** and it is not possible for operations on one variable to **affect another**.

When a value of a primitive type is **assigned to another variable** of the same type, a **copy of the primitive type** is made.

When a primitive type is passed in **to a method**, only a **copy of the primitive type** is passed. 

The called method **does not have access** to the original primitive value and therefore **cannot change it**. 

The called method can only **change the copied value**.

Primitive data types are: **byte**, **short**, **int**, **long**, **float**, **double**, **boolean** and **char**.

```Java
int i = 42; //require 4 bytes of memory
char ch = 'A'; //require 2 bytes of memory
boolean result = true; //require 1 byte of memory
```

[/slide]

[slide hideTitle]

# Reference Types

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/03.Java-Fundamentals-Methods/EN/interactive-java-fundamentals-methods-39-reference-types-and-demos-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

**Reference type** variables hold the **reference** \(pointer / memory address\) to a value.

When a reference type is **assigned to another** reference type, both will **point to the same** object.

When an object is **passed in to a method**, the called method can **change the value** of this object but **not the address** of the object.

Reference data types are: `String`, `int[]`, `char[]`, `String[]`.

```Java
String str = "Hello";
byte[] bytes = { 1, 2, 3 };
```
## Value Types Example

```java live no-template
public class MyClass {
 public static void main(String[] args) {
   int num = 5;
   increment(num, 15);
   System.out.println(num);
}

public static void increment(int num, int value) {
   num += value;
 }
}
```

## Reference Types Example

```java live no-template
public class MyClass {
public static void main(String[] args) {
  int[] nums = { 5 };
  increment(nums, 15);
  System.out.println(nums[0]);
}

public static void increment(int[] nums, int value) {
  nums[0] += value;
 }
} 
```
[/slide]

[slide hideTitle]
# Value types vs. Reference Types

[image assetsSrc="java-fund-methods-01.gif" /]

Now we will demonstrate how value types are stored, compared to reference types. 

Let us initialize some primitive value type variables, followed reference type variables:

```java
//primitives
int num = 42;
char letter = 'A';
boolean isRunning = true;

//reference type
String str = "Hello";
byte[] bytes ={ 1, 2, 3 };
```

[image assetsSrc="java-fund-methods-02.png" /]

[/slide]

[slide hideTitle]

# Example: Value Types

```java
public static void main(String[] args) {
   int num = 5;
   incrementNumber(num, 15);
   System.out.println(num);
}

public static void incrementNumber(int num, int incrementValue) {
   num += incrementValue;
}
```

We have an **incrementNumber** method that accpets two pass-in parameters: an **initial number (num)** and an **incrementValue**.

Even though we perform the `incrementNumber` method using the **num** variable, its value will not have changed when **num** is printed to the console. 

This is because **int** is a primitive type and inly a copy of its value is passed in to the method.

[/slide]

[slide hideTitle]

# Example: Reference Types


```java
public static void main(String[] args) {
  int[] nums = { 5 };
  increment(nums, 15);
  System.out.println(nums[0]);
}

public static void increment(int[] numbersArray, int incrementValue) {
  numbersArray[0] += incrementValue;
}

```

Arrays store references to memory locations. When we pass the array in to the **increment** method, it manipulates the values stored at the same memory reference. 

When we pass the **nums** array in to the method, the **numbersArray** parameter receivs the reference to the memory location of the **nums** array. 

Any operation that changes an element in the array inside the method will also change the original array as we are working with the same reference.

[/slide]


[slide hideTitle]
# Problem with Solution: Math Operations

[video src="https://videos.softuni.org/hls/Java/Java-Fundamentals-Methods-And-Arrays/03.Java-Fundamentals-Methods/EN/interactive-java-fundamentals-methods-problem-and-solution-math-operations-,1080p,720p,480p,360p,240p,.mp4/urlset/master.m3u8" poster="" /]

[code-task title="Math Operations" taskId="java-fund-1-Methods-lab-Math-Operations" executionType="tests-execution" executionStrategy="java-code" requiresInput]
[code-editor language=java]
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        // Write your code here
    }
}
```
[/code-editor]
[task-description]
## Description
Create a method that receives **two numbers** and an **operator**, calculates the result and returns it.

There will be **three lines of input**.

The first will be the first **number**, the second one will be the **operator** and the last one will be the **second number**.

The possible operators are: `/`, `*`, `+` and `-`.

## Examples
|**Input**|**Output**|
| --- | --- | 
| 5 | 25 |
| \* ||
| 5 ||

|**Input**|**Output**|
| --- | --- | 
| 4 | 12 |
| \+ ||
| 8 ||

[/task-description]
[code-io /]
[tests]
[test open]
[input]
5
\*
5
[/input]
[output]
25
[/output]
[/test]
[test open]
[input]
4
+
8
[/input]
[output]
12
[/output]
[/test]
[test]
[input]
4
/
2
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
3
\-
1
[/input]
[output]
2
[/output]
[/test]
[test]
[input]
5
+
2
[/input]
[output]
7
[/output]
[/test]
[test]
[input]
2
\*
3
[/input]
[output]
6
[/output]
[/test]
[test]
[input]
5
+
5
[/input]
[output]
10
[/output]
[/test]
[/tests]
[/code-task]
[/slide]

