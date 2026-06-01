# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Write a Java program to implement Class and Object concepts.

## AIM:
To create a class and object in Java and access class members using an object.

## ALGORITHM :
1. Start the program
2. Create a Car class with brand, model, and year attributes
3. Create two Car objects and assign values to their attributes
4. Display the details of both car objects
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
class Car
{
    String brand;
    String model;
    int year;
}
public class prog
{
    public static void main(String[] args) 
    {
        Car car1 = new Car();
        car1.brand = "Toyota";
        car1.model = "Innova";
        car1.year = 2022;

        Car car2 = new Car();
        car2.brand = "Hyundai";
        car2.model = "i20";
        car2.year = 2021;

        System.out.println("Car 1: " + car1.brand + " " + car1.model + " " + car1.year);
        System.out.println("Car 2: " + car2.brand + " " + car2.model + " " + car2.year);
    }
}
```

## OUTPUT:
<img width="571" height="233" alt="image" src="https://github.com/user-attachments/assets/7f530725-7883-4f81-83b6-0f6a17a0446f" />

## RESULT:
Thus, the Java program to implement Class and Object concepts was executed successfully.
