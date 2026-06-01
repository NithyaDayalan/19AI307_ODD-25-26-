# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to implement access specifiers.

## AIM:
To create a Java program using access specifiers with private data members and public getter and setter methods.

## ALGORITHM :
1. Start the program
2. Read the book title, author name, price, and discount percentage from the user
3. Create a Book object and set its details using setter methods
4. Apply the discount to the book price and display the updated details
5. End the program

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: NITHYA D 
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.*;
class Book {
    private String title;
    private String author;
    private double price;
    public String getTitle() { 
        return title; 
    }
    public String getAuthor() { 
        return author; 
    }
    public double getPrice() { 
        return price; 
    }
    public void setTitle(String title) { 
        this.title = title; 
    }
    public void setAuthor(String author) { 
        this.author = author; 
    }
    public void setPrice(double price) { 
        this.price = price; 
    }
    public void applyDiscount(double percentage) {
        if (percentage > 0 && percentage <= 100) {
            price = price - (price * (percentage / 100));
        }
    }
    public void display() {
        System.out.println("Title: " + title);
        System.out.println("Author: " + author);
        System.out.printf("Discounted Price: %.2f\n", price);
        System.out.println("-------------------------");
    }
}
public class java {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String title = sc.nextLine();
        String author = sc.nextLine();
        double price = sc.nextDouble();
        double discount = sc.nextDouble();
        Book book = new Book();
        book.setTitle(title);
        book.setAuthor(author);
        book.setPrice(price);
        book.applyDiscount(discount);
        book.display();
    }
}
```


## OUTPUT:
<img width="902" height="588" alt="image" src="https://github.com/user-attachments/assets/97bc42c2-1c05-48da-a431-23f7dbfb102a" />

## RESULT:
Thus, the Java program to implement access specifiers was executed successfully.
