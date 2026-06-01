# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To study and implement array concepts in Java and calculate the average of array elements.

## ALGORITHM :
1. Start the program
2. Read the number of elements n from the user
3. Read n array elements and calculate their sum
4. Find the average by dividing the sum by n and display it
5. End the program
   
## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
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
        int[] arr=new int[n];
        float avg=0;
        for(int i=0;i<n;i++)
        {
            arr[i]=sc.nextInt();
            avg+=arr[i];
        }
        System.out.printf("The average of elements is %.2f",avg/n);
    }
}
```

## OUTPUT:
<img width="768" height="505" alt="image" src="https://github.com/user-attachments/assets/21a1005c-c01e-4677-89c9-146e8df537cd" />



## RESULT:
Thus the Java program to implement arrays and calculate the average of elements was executed successfully and the output was verified.
