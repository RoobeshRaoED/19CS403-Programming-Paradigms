# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:

Print Right-Angled Triangle Star Pattern

## AIM:

To print a right-angled triangle star pattern based on the number of rows.

## ALGORITHM :

1. Read the number of rows from the user.
2. Start a loop from 1 to the number of rows.
3. For each row, print stars equal to the row number.
4. Move to the next line after printing each row.
5. End the program after printing the full triangle pattern.

## PROGRAM:

```

import java.util.Scanner;

public class RightAngledTriangle {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Input from user
        int n = sc.nextInt();

        // Print pattern
        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println();
        }

        sc.close();
    }
}

```

## OUTPUT:

![](1C.png)

## RESULT:

The program prints a right-angled triangle formed using star (*) symbols.
