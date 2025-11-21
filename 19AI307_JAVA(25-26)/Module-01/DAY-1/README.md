# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Create a class Book with attributes title, author, price. Create 2 objects and print their details.

## AIM:

Create a class Book with attributes title, author, price. Create 2 objects and print their details.

## ALGORITHM :

1.	Create a Book class with title, author, and price as attributes.

2. Write a constructor to initialize these attributes.

3. Inside main, create two Book objects with sample values.

4. Print the details of each book using System.out.println.

5. Run the program to display both books’ information.

## PROGRAM:
```

import java.util.Scanner;

class Book {
    String title;
    String author;
    double price;
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Book b1 = new Book();
        b1.title = sc.next();
        b1.author = sc.next();
        b1.price = sc.nextDouble();

        Book b2 = new Book();
        b2.title = sc.next();
        b2.author = sc.next();
        b2.price = sc.nextDouble();

        System.out.println(b1.title + " | " + b1.author + " | Rs." + b1.price);
        System.out.println(b2.title + " | " + b2.author + " | Rs." + b2.price);

        sc.close();
    }
}

```
## OUTPUT:

![](1A.png)

## RESULT:

The program creates two Book objects and prints their title, author, and price.
