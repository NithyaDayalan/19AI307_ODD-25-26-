# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create an abstract class BankAccount with a method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount to calculate interest based on the account type.

## AIM:
To implement Abstraction and Inheritance in Java by creating an abstract class BankAccount and calculating interest using its subclasses.

## ALGORITHM :
1. Start the program.
2. Create an abstract class BankAccount with an abstract method calculateInterest().
3. Create subclasses SavingsAccount and FixedDepositAccount that implement the calculateInterest() method.
4. Read the account type and required input values, create the appropriate account object, calculate the interest, and display the result.
5. End the program.
## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: NITHYA D
RegisterNumber: 212223240110
*/
```

## SOURCE CODE:
```
import java.util.*;
abstract class BankAccount 
{
    public abstract double calculateInterest();
}
class SavingsAccount extends BankAccount
{
    private double bal;
    public SavingsAccount(double bal)
    {
        this.bal=bal;
    }
    public double calculateInterest()
    {
        return bal*0.04;
    }
}
class FixedDepositAccount extends BankAccount
{
    private double amt;
    private int yrs;
    public FixedDepositAccount(double amt,int yrs)
    {
        this.amt=amt;
        this.yrs=yrs;
    }
    public double calculateInterest()
    {
        return amt*0.07*yrs;
    }
}
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int in=sc.nextInt();
        BankAccount acc;
        if(in==1)
        {
            double bal=sc.nextDouble();
            acc=new SavingsAccount(bal);
        }
        else
        {
            double amt=sc.nextDouble();
            int yrs=sc.nextInt();
            acc=new FixedDepositAccount(amt,yrs);
        }
        double i=acc.calculateInterest();
        System.out.printf("%.2f",i);
    }
}
```

## OUTPUT:
<img width="398" height="391" alt="image" src="https://github.com/user-attachments/assets/c0f557fe-68df-4f67-b018-5344eb41d422" />

## RESULT:
Thus, the Java program to demonstrate Abstraction and Inheritance by creating a BankAccount abstract class and calculating interest using its subclasses was implemented successfully and the output was verified.
