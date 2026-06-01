# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class.

## AIM:
To implement a private inner class in Java and access its functionality through a method of the outer class.

## ALGORITHM :
1. Start the program.
2. Create an outer class containing a private inner class with a display method.
3. Create a method in the outer class to instantiate and access the private inner class.
4. Read an integer value from the user and call the outer class method to display the value.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class OuterClass{

    private class InnerClass{

        void display(int data){
            System.out.println("Data set inside private inner class: " + data);
        }
    }

    void accessInner(int value){

        InnerClass obj = new InnerClass();
        obj.display(value);
    }
}

public class Main{

    public static void main(String[] args){

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        OuterClass obj = new OuterClass();
        obj.accessInner(n);

        sc.close();
    }
}
```

## OUTPUT:
<img width="863" height="335" alt="image" src="https://github.com/user-attachments/assets/e0a52151-aa98-45e3-98a5-b4759e50c9a8" />

## RESULT:
Thus, the Java program to demonstrate a private inner class accessed through a method of the outer class was implemented successfully and the output was verified.
