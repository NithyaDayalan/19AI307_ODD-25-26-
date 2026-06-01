# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a Java program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To implement Exception Handling in Java by performing division and handling the ArithmeticException that occurs when dividing by zero.

## ALGORITHM :
1.	Start the program.
2.	Read two integer values from the user.
3.	Perform the division operation inside a try block.
4.	If division by zero occurs, catch the exception and display an error message; otherwise, display the result.
5.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class DivisionExample {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

       
        int num1 = scanner.nextInt();

        
        int num2 = scanner.nextInt();

        try {
            int result = num1 / num2;
            System.out.println("Result: " + result);
        } catch (ArithmeticException e) {
            System.out.println("Error: Division by zero");
        }

        scanner.close();
    }
}
```

## OUTPUT:
<img width="666" height="363" alt="image" src="https://github.com/user-attachments/assets/6d7dd517-e358-4cac-b9aa-c456632c55ec" />

## RESULT:
Thus, the Java program to perform division and handle division by zero using Exception Handling was implemented successfully and the output was verified.
