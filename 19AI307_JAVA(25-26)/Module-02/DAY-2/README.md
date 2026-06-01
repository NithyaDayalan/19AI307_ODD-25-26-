# Ex.No:2(B) METHODS

## QUESTION:
Write a Java program to implement methods.

## AIM:
To create and use methods in Java for checking whether a method is static or non-static.

## ALGORITHM :
1. Start the program
2. Define a class with a static method and a non static method
3. Create an object of the class
4. Call the static method using the class name and the non static method using the object
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
class method
{
    static void staticMethod()
    {
        System.out.println("I am static");
    }
    void nonStaticMethod()
    {
        System.out.println("I am non-static");
    }
}
class prog
{
    public static void main(String[] args)
    {
        method m=new method();
        method.staticMethod();
        m.nonStaticMethod();
    }
}
```

## OUTPUT:
<img width="393" height="227" alt="image" src="https://github.com/user-attachments/assets/92c293fe-9115-478d-9c34-b74057494c84" />

## RESULT:
Thus, the Java program to implement methods was executed successfully.
