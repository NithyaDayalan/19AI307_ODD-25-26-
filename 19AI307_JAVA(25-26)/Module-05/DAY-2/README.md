# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to read multiple UTF strings from the user, write them to a ByteArrayOutputStream using a DataOutputStream, and display the byte array contents and stored strings.

## AIM:
To implement in-memory byte stream operations in Java using ByteArrayOutputStream, DataOutputStream, ByteArrayInputStream, and DataInputStream for storing and retrieving UTF strings.

## ALGORITHM :
1.	Start the program.
2.	Read the number of strings and store each string in a ByteArrayOutputStream using a DataOutputStream.
3.	Convert the stored data into a byte array and display its contents and total size.
4.	Read the strings back from memory using a ByteArrayInputStream and DataInputStream, then display them.
5.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class UTFStringsInMemoryUserInput {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        try {
            ByteArrayOutputStream baos = new ByteArrayOutputStream();
            DataOutputStream dos = new DataOutputStream(baos);
            int n = scanner.nextInt();
            scanner.nextLine();
            for (int i = 0; i < n; i++) {
                String str = scanner.nextLine();
                dos.writeUTF(str);
            }
            byte[] byteData = baos.toByteArray();
            System.out.println("Byte array contents:");
            for (byte b : byteData) {
                System.out.print(b + " ");
            }
            System.out.println("\nTotal bytes: " + byteData.length);
            ByteArrayInputStream bais = new ByteArrayInputStream(byteData);
            DataInputStream dis = new DataInputStream(bais);

            System.out.println("\nStrings read from memory:");
            for (int i = 0; i < n; i++) {
                System.out.println(dis.readUTF());
            }

            // Close streams
            dos.close();
            dis.close();

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        }

        scanner.close();
    }
}
```

## OUTPUT:
<img width="955" height="542" alt="image" src="https://github.com/user-attachments/assets/3330802a-4b30-4289-8831-61d6db5e2abc" />

## RESULT:
Thus, the Java program to store and retrieve multiple UTF strings using byte array streams and data streams was implemented successfully and the output was verified.
