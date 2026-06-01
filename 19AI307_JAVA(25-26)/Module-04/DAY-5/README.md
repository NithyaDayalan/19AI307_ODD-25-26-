# Ex.No:4(E) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Write a Java program using the MVC Design Pattern where a Product model stores item information, a view displays the product details, and a controller updates the product price and refreshes the view.

## AIM:
To implement the MVC Design Pattern in Java by separating the Product data, user interface, and control logic into Model, View, and Controller components.

## ALGORITHM :
1.	Start the program.
2.	Create a Product model class to store the product name, price, and code.
3.	Create a ProductView class to display the product details and a ProductController class to manage updates.
4.	Read the product details and new price, display the product information, update the price through the controller, and refresh the view.
5.	End the program.
   
## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class ProductManagementSystem {

    // ===== Model =====
    static class Product {
        private String name;
        private double price;
        private String code;

        // Constructor to initialize name, price, code
        public Product(String name, double price, String code) {
            this.name = name;
            this.price = price;
            this.code = code;
        }

        public String getName() {
            return name;
        }
        public double getPrice() {
            return price;
        }

        public String getCode() {
            return code;
        }

        public void setPrice(double price) {
            this.price = price;
        }
    }
    static class ProductView {
        public void displayProduct(String name, double price, String code) {
            System.out.println("--- Product Details ---");
            System.out.println("Name : " + name);
            System.out.println("Price: " + price);
            System.out.println("Code : " + code);
        }
    }

    static class ProductController {
        private Product product;
        private ProductView view;
        public ProductController(Product product, ProductView view) {
            this.product = product;
            this.view = view;
        }
        public void updateView() {
            view.displayProduct(product.getName(), product.getPrice(), product.getCode());
        }
        public void updatePrice(double newPrice) {
            product.setPrice(newPrice);
            updateView();
        }
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        double price = sc.nextDouble();
        String code = sc.next();
        double newPrice = sc.nextDouble();
        Product product = new Product(name, price, code);
        ProductView view = new ProductView();
        ProductController controller = new ProductController(product, view);
        controller.updateView();
        controller.updatePrice(newPrice);

        sc.close();
    }
}
```

## OUTPUT:
<img width="492" height="310" alt="image" src="https://github.com/user-attachments/assets/4f36a7ba-1856-4abe-ad34-b585bec67bbe" />

## RESULT:
Thus, the Java program to demonstrate the MVC Design Pattern by managing product information and updating product prices through a controller was implemented successfully and the output was verified.
