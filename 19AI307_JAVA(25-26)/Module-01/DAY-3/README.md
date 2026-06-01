# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program to reverse a number using looping statements.

## AIM:
To study and implement looping statements in Java using the while loop.

## ALGORITHM :
1. Start the program
2. Read an integer value n from the user
3. Reverse the number by repeatedly extracting the last digit and adding it to the reversed number
4. Display the reversed number
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
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
        int rev=0,rem=0;
        while(n>0)
        {
            rem=n%10;
            rev=rev*10+rem;
            n/=10;
        }
        System.out.println("Reversed number: "+rev);
    }
}
```

## OUTPUT:
<img width="555" height="311" alt="image" src="https://github.com/user-attachments/assets/68c8cd3d-9b4a-4c1a-a96c-a1ce6d14c999" />

## RESULT:
Thus the Java program to implement looping statements using the while loop was executed successfully and the output was verified.
