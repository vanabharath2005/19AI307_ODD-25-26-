# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Employee with method display(). Inside display(), return the current object using this. Create another method that calls display().printName()

## AIM:
To write a Java program that demonstrates returning the current object using this inside a method. The program should include a method display() that returns the current object and another method that calls display().printName() to show how method chaining works.



## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util' 3.Create a class named Employee.
Inside the class, declare an instance variable name.
Create a constructor to initialize the employee name.
Define a method display() that:
Prints a message.
Returns the current object using return this;
Define a method printName() that prints the employee name.
Create another method (e.g., show()) that calls display().printName() to demonstrate method chaining.
In the main method:
Create an object of Employee.
Call the show() method.
```





## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:

```
import java.util.*;
class Employee
{
    String name;
    void setName(String name)
    {
        this.name = name;
    }
    Employee display()
    {
        return this;
    }
    void printName()
    {
        System.out.println("Employee Name: " + name);
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String empName = sc.nextLine();  
        Employee obj = new Employee();
        obj.setName(empName);
        obj.display().printName();
    }
}
```





## OUTPUT:

<img width="705" height="217" alt="image" src="https://github.com/user-attachments/assets/bf5f2ba3-35c1-446c-948a-8446bd4ebec5" />



## RESULT:
The program successfully demonstrates returning the current object using this inside a method. It also shows how method chaining works by calling display().printName().
