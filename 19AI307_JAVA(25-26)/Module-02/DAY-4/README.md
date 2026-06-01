# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to implement variable scope and constructor.

## AIM:
To create a Java program that demonstrates variable scope and the use of constructors.

## ALGORITHM :
1. Start the program
2. Read the student's name and age from the user
3. Create a Student object using the constructor and initialize the data members
4. Display the student details using the toString method
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Student {
    private String name;
    private int age;

    public Student(String name, int age) {
        this.name = name;
        this.age = age;
    }

    @Override
    public String toString() {
        return "Student{name='" + name + "', age=" + age + "}";
    }
}

public class StudentTest {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();

        Student s = new Student(name, age);

        System.out.println(s);

        sc.close();
    }
}
```

## OUTPUT:
<img width="705" height="347" alt="image" src="https://github.com/user-attachments/assets/0fef1c88-868d-4fdc-acf8-0d851947f788" />

## RESULT:
Thus, the Java program to implement variable scope and constructor was executed successfully.
