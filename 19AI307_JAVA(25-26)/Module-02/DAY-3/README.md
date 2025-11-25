# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:

Write a Java program to create a class called Employee with private instance variables employee_id, employee_name, and employee_salary. Provide public getter and setter methods to access and modify the id and name variables, but provide a getter method for the salary variable that returns a formatted string 
```
public class Employee {
    
    private int employee_id;
    private String employee_name;
    private double employee_salary;

    
    public int getEmployeeId() {
        return employee_id;
    }
    public void setEmployeeId(int employee_id) {
        this.employee_id = employee_id;
    }

    
    public String getEmployeeName() {
        return employee_name;
    }
    public void setEmployeeName(String employee_name) {
        this.employee_name = employee_name;
    }

  
    public void setEmployeeSalary(double employee_salary) {
        this.employee_salary = employee_salary;
    }

   
    public String getFormattedSalary() {
        return String.format("₹%.2f", employee_salary);
    }
}
```

## AIM:

Create an Employee class with encapsulated fields and a formatted salary getter.

## ALGORITHM :

1. Declare private variables for id, name, and salary.
2. Implement public getters and setters for id and name.
3. Implement a setter for salary without exposing it directly.
4. Implement a getter that returns salary using String.format().
5. Compile and test to ensure proper encapsulation and formatted output.

## PROGRAM:

```

import java.util.Scanner;

public class Employee {
    private int employee_id;
    private String employee_name;
    private double employee_salary;

    public int getEmployeeId() {
        return employee_id;
    }
    public void setEmployeeId(int employee_id) {
        this.employee_id = employee_id;
    }

    public String getEmployeeName() {
        return employee_name;
    }
    public void setEmployeeName(String employee_name) {
        this.employee_name = employee_name;
    }

    public void setEmployeeSalary(double employee_salary) {
        this.employee_salary = employee_salary;
    }

    public String getFormattedSalary() {
        return String.format("₹%.2f", employee_salary);
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Employee emp = new Employee();

        emp.setEmployeeId(sc.nextInt());
        sc.nextLine(); // consume newline
        emp.setEmployeeName(sc.nextLine());
        emp.setEmployeeSalary(sc.nextDouble());
        
        System.out.println("Employee 1");
        System.out.println("ID: " + emp.getEmployeeId());
        System.out.println("Name: " + emp.getEmployeeName());
        System.out.println("Salary: " + emp.getFormattedSalary());
        sc.close();
    }
}

```

## OUTPUT:

![](2C.png)

## RESULT:

Employee class created with proper encapsulation and formatted salary retrieval.

