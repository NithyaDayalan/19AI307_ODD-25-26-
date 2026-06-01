# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to demonstrate chaining of streams using BufferedReader on top of InputStreamReader on top of System.in.

## AIM:
To implement stream chaining in Java by using a BufferedReader wrapped around an InputStreamReader to read user input efficiently.

## ALGORITHM :
1. Start the program.
2. Create a BufferedReader object by wrapping an InputStreamReader around System.in.
3. Read the user's name and age from the input stream.
4. Display the entered user details.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample 
{
    public static void main(String[] args)
    {
        
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        try 
        {
            String name = br.readLine(); 
            int age = Integer.parseInt(br.readLine()); 

            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);
        } catch (IOException e) {
            System.out.println("An error occurred while reading input.");
        }
    }
}
```

## OUTPUT:
<img width="470" height="376" alt="image" src="https://github.com/user-attachments/assets/e7e98f97-8f18-4314-825e-f9cba203b16d" />

## RESULT:
Thus, the Java program to demonstrate chaining of streams using BufferedReader, InputStreamReader, and System.in was implemented successfully and the output was verified.
