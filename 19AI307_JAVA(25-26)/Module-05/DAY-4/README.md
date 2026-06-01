# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a Java program to set the name and priority of two threads. Read the thread names from the user and set the priority as 4 for t1 and 2 for t2.

## AIM:
To implement thread management in Java by creating threads, assigning names, setting priorities, and displaying thread information.

## ALGORITHM :
1.	Start the program.
2.	Read the names of two threads from the user.
3.	Create two thread objects and assign the entered names to them.
4.	Set the priority of the first thread to 4 and the second thread to 2, then display their details.
5.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.util.*;

public class ThreadPriorityExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        t1.setName(name1);
        t2.setName(name2);
        t1.setPriority(4);
        t2.setPriority(2);
        System.out.println(t1);
        System.out.println(t2);

        sc.close();
    }
}
```

## OUTPUT:
<img width="626" height="183" alt="image" src="https://github.com/user-attachments/assets/f67577c0-3b52-4b9d-9a1b-1a1b5c0ec380" />

## RESULT:
Thus, the Java program to set the name and priority of threads and display their details was implemented successfully and the output was verified.
