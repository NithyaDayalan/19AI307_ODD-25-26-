# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to reverse a number using the Integer wrapper class and compare it with the original number to determine whether it is a palindrome.

## AIM:
To implement the Integer Wrapper Class in Java and check whether a given number is a palindrome by reversing its digits.

## ALGORITHM :
1.	Start the program.
2.	Read an integer value using the Integer wrapper class and store the original number.
3.	Reverse the number by repeatedly extracting its digits and forming the reversed number.
4.	Compare the reversed number with the original number and display whether it is a palindrome. If not, display the reversed number.
5.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main{

    public static void main(String[] args){

        Scanner sc = new Scanner(System.in);

        Integer num = sc.nextInt();

        int original = num;
        int reverse = 0;

        while(num > 0){

            int digit = num % 10;
            reverse = reverse * 10 + digit;
            num = num / 10;
        }

        if(original == reverse){
            System.out.println(original + " is a palindrome number.");
        }
        else{
            System.out.println(original + " is not a palindrome number.");
            System.out.println("Reversed Number: " + reverse);
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="738" height="345" alt="image" src="https://github.com/user-attachments/assets/40fe6aa9-b553-4f17-aa91-9a2606806d09" />

## RESULT:
Thus, the Java program to reverse a number using the Integer Wrapper Class and check whether it is a palindrome was implemented successfully and the output was verified.
