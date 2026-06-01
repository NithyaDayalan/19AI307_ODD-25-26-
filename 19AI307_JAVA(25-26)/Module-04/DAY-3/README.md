# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Write a Java program to implement Composition where a Library contains multiple Book objects. Books are created inside the Library and cannot exist independently.

## AIM:
To implement the concept of Composition in Java by creating a Library class that contains and manages multiple Book objects.

## ALGORITHM :
1.	Start the program.
2.	Create a Book class with title and author attributes and a method to display book details.
3.	Create a Library class that maintains a collection of Book objects and provides methods to add and display books.
4.	Read the book details from the user, create books through the Library class, and display all books in the library.
5.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
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

    // Constructor
    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    // Method to display book details
    public void displayBook() {
        System.out.println("- " + title + " by " + author);
    }
}

class Library {
    private List<Book> books;

    // Constructor initializes the list of books
    public Library() {
        books = new ArrayList<>();
    }

    // Method to add a book (book is created inside the Library)
    public void addBook(String title, String author) {
        Book book = new Book(title, author);
        books.add(book);
    }

    // Method to display all books in the library
    public void displayBooks() {
        System.out.println("Books in Library:");
        for (Book book : books) {
            book.displayBook();
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Create Library object
        Library library = new Library();

        int n = sc.nextInt();  // number of books to add
        sc.nextLine(); // consume newline

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.displayBooks();
    }
}
```

## OUTPUT:
<img width="676" height="465" alt="image" src="https://github.com/user-attachments/assets/b6accbf2-2c79-4b90-b679-209ea6777ea4" />

## RESULT:
Thus, the Java program to demonstrate Composition by creating a Library that contains multiple Book objects was implemented successfully and the output was verified.
