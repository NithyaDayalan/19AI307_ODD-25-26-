# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Write a Java program to implement conditional statements using if-else conditions.

## AIM:
To study and implement conditional statements in Java using if, else if, and else constructs.

## ALGORITHM :
1. Start the program
2. Read an integer value n from the user
3. Check whether n is even and less than 100. If true, display Weak Code
4. Otherwise, check whether n is even and between 100 and 999. If true, display Strong Code, else display Access Denied
5. End the program


## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.*;
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        if(n%2==0)
        {
            if(n<100)
            {
                System.out.println("Weak Code");
            }
            else if(n>=100&&n<1000)
            {
                System.out.println("Strong Code");
            }
        }
        else
        {
            System.out.println("Access Denied");
        }
        if(n>=1000)
        {
            System.out.println("Access Denied");
        }
    }
}
```

## OUTPUT:
<img width="405" height="324" alt="image" src="https://github.com/user-attachments/assets/427e775d-28a8-4b61-8a45-48503e9cc44c" />

## RESULT:
Thus the Java program to implement conditional statements using if-else conditions was executed successfully and the output was verified.
