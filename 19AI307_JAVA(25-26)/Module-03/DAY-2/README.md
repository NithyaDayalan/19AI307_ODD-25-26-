# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to calculate the area of a square, rectangle, and circle using method overloading.

## AIM:
To implement Method Overloading in Java by calculating the area of different shapes such as square, rectangle, and circle using overloaded methods.

## ALGORITHM :
1. Start the program.
2. Create a class AreaCalculator with overloaded area() methods for square, rectangle, and circle.
3. Read the side of the square, length and breadth of the rectangle, and radius of the circle.
4. Call the appropriate overloaded methods and display the calculated areas.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.*;
class AreaCalculator 
{
    int area(int side) 
    {
        return side * side;
    }
    int area(int length, int breadth) 
    {
        return length * breadth;
    }
    double area(double radius) 
    {
        return Math.PI * radius * radius;
    }
}
public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        AreaCalculator calc = new AreaCalculator();
        int side = sc.nextInt();
        System.out.println("Area of square: " + calc.area(side));
        int length = sc.nextInt();
        int breadth = sc.nextInt();
        System.out.println("Area of rectangle: " + calc.area(length, breadth));
        double radius = sc.nextDouble();
        System.out.println("Area of circle: " + calc.area(radius));
    }
}
```

## OUTPUT:
<img width="746" height="418" alt="image" src="https://github.com/user-attachments/assets/569db0d9-616a-400d-9065-cb7ea8a048c9" />

## RESULT:
Thus, the Java program to calculate the area of different shapes using Method Overloading was implemented successfully and the output was verified.
