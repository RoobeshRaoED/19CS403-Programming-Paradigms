# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:

Create a class Utility with a static method square(int num) that returns the square of a number. Call the method without creating an object. 

```
import java.util.Scanner;
class Utility {

    static int square(int num) {
        // Return the square of the number
    }
}
class prog {
    public static void main(String[] args) {
       // Main Method
    }
}
```

## AIM:

Create a class with a static square() method and call it without creating an object.

## ALGORITHM :

1. Create a class Utility with a static method square(int num).
2. Implement the method to return num * num.
3. In main(), read an integer using Scanner.
4. Call Utility.square(value) directly without an object.
5. Print the returned result.

## PROGRAM:

```

import java.util.Scanner;

class Utility {

    static int square(int num) {
        // Return the square of the number
        return num * num;
    }
}

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.println(Utility.square(n)); // Calling without object
        sc.close();
    }
}

```

## OUTPUT:

![](2E.png)

## RESULT:

Static square method executed successfully without creating an object.

