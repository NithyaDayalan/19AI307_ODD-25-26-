# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a Java program to implement access modifiers.

## AIM:
To create a Java program that demonstrates the use of access modifiers in Java.

## ALGORITHM :
1. Start the program
2. Display the message Calculator is ready using the static method
3. Read two integer values from the user
4. Create a Calculator object, find the sum of the two numbers, and display the result
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Calculator {

    public int add(int a, int b) {
        return a + b;
    }

    public static void info() {
        System.out.println("Calculator is ready");
    }
}

class prog {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        Calculator.info();

        int x = sc.nextInt();
        int y = sc.nextInt();

        Calculator calc = new Calculator();

        int sum = calc.add(x, y);

        System.out.println("Sum: " + sum);

        sc.close();
    }
}
```

## OUTPUT:
<img width="543" height="342" alt="image" src="https://github.com/user-attachments/assets/0094e549-62d6-464a-ae8d-4ab838c28d3d" />

## RESULT:
Thus, the Java program to implement access modifiers was executed successfully.
