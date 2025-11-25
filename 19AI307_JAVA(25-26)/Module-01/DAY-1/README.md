# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Lovely found a magic machine that tells her how two numbers relate to each other.
The machine supports all 6 relational operators:

Operator	Meaning

==	Is equal to

!=	Is not equal to

>	Greater than

<	Less than

>=	Greater than or equal to

<=	Less than or equal to

Lovely enters two numbers. The machine prints the result (true or false) for each operator.

Input Format

First line: First integer number (a)

Second line: Second integer number (b)

Output Format

Print:

a == b: <true/false>

a != b: <true/false>

a > b: <true/false>

a < b: <true/false>

a >= b: <true/false>

a <= b: <true/false>

## AIM:

To compare two integers using all six relational operators and display the results.

## ALGORITHM :

1. Read two integer inputs a and b from the user.
2. Compare a and b using the equality and inequality operators.
3. Compare a and b using greater-than and less-than operators.
4. Print the result of each comparison in the required format.
5. End the program after displaying all six relational comparison results.

## PROGRAM:
```

import java.util.*;

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();

        System.out.println("a == b: " + (a == b));
        System.out.println("a != b: " + (a != b));
        System.out.println("a > b: " + (a > b));
        System.out.println("a < b: " + (a < b));
        System.out.println("a >= b: " + (a >= b));
        System.out.println("a <= b: " + (a <= b));
    }
}

```
## OUTPUT:

![](1A.png)

## RESULT:

The program outputs true/false for all relational comparisons between the two integers.

