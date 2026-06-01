# Ex.No:3(D)    INTERFACE 

## QUESTION:
Write a Java program to create a WeatherBot interface and implement it using SunBot and RainBot classes to predict weather conditions based on temperature.

## AIM:
To implement the concept of Interfaces in Java by creating different weather prediction bots that provide predictions based on temperature.

## ALGORITHM :
1. Start the program.
2. Create an interface WeatherBot with the method predict().
3. Implement the interface in SunBot and RainBot classes with their respective prediction logic.
4. Read the temperature and bot type, create the appropriate bot object, and display the prediction.
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.*;
interface WeatherBot
{
    String predict(int temp);
}
class SunBot implements WeatherBot
{
    public String predict(int temp)
    {
        if(temp>30)
        {
            return "HOT";
        }
        else
        {
            return "MODERATE";
        }
    }
}
class RainBot implements WeatherBot
{
    public String predict(int temp)
    {
        if(temp<20)
        {
            return "COLD";
        }
        else
        {
            return "WARM";
        }
    }
}
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int temp=sc.nextInt();
        int bot=sc.nextInt();
        WeatherBot w;
        if(bot==1)
        {
            w=new SunBot();
        }
        else
        {
            w=new RainBot();
        }
        System.out.println(w.predict(temp));
    }
}
```

## OUTPUT:
<img width="318" height="227" alt="image" src="https://github.com/user-attachments/assets/42da1fef-b18a-4d8f-845d-958256c5e51c" />

## RESULT:
Thus, the Java program to demonstrate Interfaces by creating SunBot and RainBot classes implementing the WeatherBot interface was implemented successfully and the output was verified.
