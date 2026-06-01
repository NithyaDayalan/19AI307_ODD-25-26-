# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a Java program to overwrite the content of a file.

## AIM:
To implement file handling in Java by overwriting the existing content of a file using the FileWriter class.

## ALGORITHM :
1.	Start the program.
2.	Read the content to be written from the user.
3.	Create a FileWriter object in overwrite mode and write the content to the file.
4.	Close the file and display a success message.
5.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

public class OverwriteFileExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String content = sc.nextLine();
        
        try {
           
            FileWriter writer = new FileWriter("output.txt", false);
            writer.write(content);
            writer.close();
            
            System.out.println("File content overwritten successfully.");
        } 
        catch (IOException e) {
            System.out.println("An error occurred.");
            e.printStackTrace();
        }
        
        sc.close();
    }
}
```

## OUTPUT:
<img width="862" height="163" alt="image" src="https://github.com/user-attachments/assets/4d246b90-8811-4f4f-9c9d-c0488478cc06" />

## RESULT:
Thus, the Java program to overwrite the content of a file using FileWriter was implemented successfully and the output was verified.
