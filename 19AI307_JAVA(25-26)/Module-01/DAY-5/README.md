# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program to reverse a given string and implement it.

## ALGORITHM :
1. Start the program
2. Read a string from the user
3. Reverse the string by traversing it from the last character to the first character
4. Display the reversed string
5. End the program


## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
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
        String s=sc.next();
        String rev="";
        for(int i=s.length()-1;i>=0;i--)
        {
            rev=rev+s.charAt(i);
        }
        System.out.println("Reversed string: "+rev);
    }
}
```

## OUTPUT:
<img width="611" height="295" alt="image" src="https://github.com/user-attachments/assets/14522870-bb36-4132-a890-ce656f8f14b4" />


## RESULT:
The java program the reverse the string is implemented and executed successfully.
