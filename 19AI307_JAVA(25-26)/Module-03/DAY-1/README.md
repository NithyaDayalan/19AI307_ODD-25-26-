# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks.

## AIM:
To implement Inheritance in Java by creating a Person superclass and a Student subclass, and to calculate the grade based on student marks.

## ALGORITHM :
1. Start the program.
2. Create a superclass Person with fields name and age.
3. Create a subclass Student that inherits from Person, adds a marks field, and implements the calculateGrade() method.
4. Read the student's name, age, and marks, calculate the grade, and display all details.
5. End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person
{
    String name;
    int age;
}
class Student extends Person
{
    int marks;
    char calculateGrade()
    {
        if (marks>=90)
        {
            return 'A';
        }
        else if(marks>=75&&marks<90)
        {
            return 'B';
        }
        else if(marks>=50&&marks<75)
        {
            return 'C';
        }
        else
        {
            return 'F';
        }
    }
}
class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        Student s=new Student();
        s.name=sc.next();
        s.age=sc.nextInt();
        s.marks=sc.nextInt();
        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        System.out.println("Grade: " + s.calculateGrade());
    }
}
```

## OUTPUT:
<img width="505" height="590" alt="image" src="https://github.com/user-attachments/assets/e90c77a9-312d-461c-8046-5cc38f62e43d" />

## RESULT:
Thus, the Java program to demonstrate Inheritance by creating a Person superclass and a Student subclass, and calculating the grade based on marks, was implemented successfully and the output was verified.
