# Ex.No:3(B) POLYMORPHISM

## QUESTION:

 Write a Java program to create a class Vehicle with a method called speedUp(). Create two subclasses Car and Bicycle. Override the speedUp() method in each subclass to increase the vehicle's speed differently.

## AIM:

To demonstrate method overriding by creating a Vehicle class with a speedUp() method and overriding it in Car and Bicycle subclasses.

## ALGORITHM :

1. Create a parent class Vehicle with a method speedUp().
2. Create two subclasses Car and Bicycle that extend Vehicle.
3. Override the speedUp() method in both subclasses with different implementations.
4. In the main method, create objects of Car and Bicycle.
5. Call the speedUp() method on each object to display their specific behavior.

## PROGRAM:

```

import java.util.Scanner;

class Vehicle {
    void speedUp(int speed) {
        System.out.println("Vehicle speed increased to: " + speed + " km/h");
    }
}

class Car extends Vehicle {
    @Override
    void speedUp(int speed) {
        System.out.println("Car speed increased to: " + (speed * 2) + " km/h");
    }
}

class Bicycle extends Vehicle {
    @Override
    void speedUp(int speed) {
        System.out.println("Bicycle speed increased to: " + speed + " km/h");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().toLowerCase();
        int speed = sc.nextInt();

        Vehicle v;
        if (type.equals("car")) {
            v = new Car();
        } else if (type.equals("bicycle")) {
            v = new Bicycle();
        } else {
            v = new Vehicle();
        }

        v.speedUp(speed);
    }
}

```

## OUTPUT:

![](3B.png)

## RESULT:

The program shows different speedUp() behaviors for Car and Bicycle using method overriding.
