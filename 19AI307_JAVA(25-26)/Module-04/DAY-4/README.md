# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Write a Java program using the Abstract Factory Design Pattern to create Button and Checkbox components for Dark and Light themes based on user selection.

## AIM:
To implement the Abstract Factory Design Pattern in Java by creating theme-specific Button and Checkbox UI components for Dark and Light themes.

## ALGORITHM :
1.	Start the program.
2.	Create interfaces for Button, Checkbox, and UIFactory.
3.	Implement concrete product classes and concrete factory classes for Dark and Light themes.
4.	Read the theme from the user, create the appropriate factory, generate the UI components, and display their types.
5.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: NITHYA D
RegisterNumber: 212223240110 
*/
```

## SOURCE CODE:
```
import java.util.*;
interface Button 
{
    void paint();
}

interface Checkbox
{
    void paint();
}
class DarkButton implements Button 
{
    public void paint()
    {
        System.out.println("Dark Button created");
    }
}

class DarkCheckbox implements Checkbox {
    public void paint() {
        System.out.println("Dark Checkbox created");
    }
}
class LightButton implements Button 
{
    public void paint() 
    {
        System.out.println("Light Button created");
    }
}

class LightCheckbox implements Checkbox
{
    public void paint() 
    {
        System.out.println("Light Checkbox created");
    }
}
interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}
class DarkThemeFactory implements UIFactory 
{
    public Button createButton() 
    {
        return new DarkButton();
    }

    public Checkbox createCheckbox() {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() {
        return new LightButton();
    }

    public Checkbox createCheckbox() {
        return new LightCheckbox();
    }
}

class FactoryProducer {
    public static UIFactory getFactory(String theme) {
        if (theme.equalsIgnoreCase("dark")) {
            return new DarkThemeFactory();
        } else if (theme.equalsIgnoreCase("light")) {
            return new LightThemeFactory();
        }
        return null;
    }
}
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String theme = sc.nextLine().trim();
        UIFactory factory = FactoryProducer.getFactory(theme);

        if (factory != null) {
            Button button = factory.createButton();
            Checkbox checkbox = factory.createCheckbox();
            button.paint();
            checkbox.paint();
        } else {
            System.out.println("Invalid theme");
        }
        sc.close();
    }
}
```

## OUTPUT:
<img width="480" height="277" alt="image" src="https://github.com/user-attachments/assets/aa94027e-9b7b-4194-bad4-8053f62c7fef" />

## RESULT:
Thus, the Java program to demonstrate the Abstract Factory Design Pattern by creating theme-specific Button and Checkbox components was implemented successfully and the output was verified.
