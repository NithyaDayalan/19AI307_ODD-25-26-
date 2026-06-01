# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Write a Java program to read N numbers from the user and use a fixed thread pool of size 3 to compute twice the value of each number and display the results in order.

## AIM:
To implement multithreading in Java using a Fixed Thread Pool and Future objects to process tasks concurrently and retrieve results in order.

## ALGORITHM :
1.	Start the program.
2.	Read the number of tasks and the input numbers from the user.
3.	Create a fixed thread pool of size 3 and submit tasks to multiply each number by 2.
4.	Retrieve the results using Future objects and display them in the same order as the input.
5.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.util.*;
import java.util.concurrent.*;

public class FixedThreadPoolTask {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int T = sc.nextInt();
        List<Integer> numbers = new ArrayList<>();
        for (int i = 0; i < T; i++) {
            numbers.add(sc.nextInt());
        }
        ExecutorService executor = Executors.newFixedThreadPool(3);
        List<Future<Integer>> results = new ArrayList<>();

        for (int num : numbers) {
            Future<Integer> result = executor.submit(() -> num * 2);
            results.add(result);
        }
        for (Future<Integer> res : results) {
            try {
                System.out.println("Result: " + res.get());
            } catch (Exception e) {
                e.printStackTrace();
            }
        }

        executor.shutdown();
        sc.close();
    }
}
```

## OUTPUT:
<img width="323" height="345" alt="image" src="https://github.com/user-attachments/assets/d6e249e8-c33a-450d-8ee4-8ad7eba39bdd" />

## RESULT:
Thus, the Java program to process tasks using a Fixed Thread Pool and display the results in order was implemented successfully and the output was verified.
