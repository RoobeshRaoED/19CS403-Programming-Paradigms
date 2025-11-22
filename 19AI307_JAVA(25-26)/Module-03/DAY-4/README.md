# Ex.No:3(D)    INTERFACE 

## QUESTION:

Schools use different grading schemes. You need to build a system to plug different strategies.

SimpleGrader: A: 90+, B: 75–89, C: 60–74, F: below 60

StrictGrader: A: 95+, B: 85–94, C: 70–84, F: below 70

Input Format:
marks
graderType
marks: Integer (0–100)

graderType: 1 for SimpleGrader, 2 for StrictGrader

Output Format:
A / B / C / F

## AIM:

To implement a grading system that selects between SimpleGrader and StrictGrader strategies based on user input.

## ALGORITHM :

1. Create a Grader interface with a method grade(int marks).
2. Implement SimpleGrader to classify marks using: A(90+), B(75–89), C(60–74), F(<60).
3. Implement StrictGrader to classify marks using: A(95+), B(85–94), C(70–84), F(<70).
4. Read marks and graderType as input.
5. Create the chosen grader object, call grade(), and print the resulting grade.

## PROGRAM:

```

import java.util.*;

abstract class Grader {
    abstract char grade(int marks);
}

class SimpleGrader extends Grader {
    @Override
    char grade(int marks) {
        if (marks >= 90) return 'A';
        else if (marks >= 75) return 'B';
        else if (marks >= 60) return 'C';
        else return 'F';
    }
}

class StrictGrader extends Grader {
    @Override
    char grade(int marks) {
        if (marks >= 95) return 'A';
        else if (marks >= 85) return 'B';
        else if (marks >= 70) return 'C';
        else return 'F';
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();
        int type = sc.nextInt();

        Grader grader;
        if (type == 1)
            grader = new SimpleGrader();
        else
            grader = new StrictGrader();

        System.out.println(grader.grade(marks));
        sc.close();
    }
}

```

## OUTPUT:

![](3D.png)

## RESULT:

The system outputs the grade according to the selected grading strategy.
