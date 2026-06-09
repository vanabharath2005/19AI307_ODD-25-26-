# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:


## AIM:
# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables

## AIM:
To write a Java program that defines a class Person with private instance variables name, age, and country, and to provide public getter and setter methods to access and modify these variables.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Create a class named Person.
Declare private instance variables:
name (String)
age (int)
country (String)
Define public setter methods to assign values to each variable.
Define public getter methods to retrieve the values of each variable.
In the main method:
Create an object of the Person class.
Use setter methods to set name, age, and country.
Use getter methods to display the values.
End the program.
```






## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.util.*;
class Person
{
    private String name;
    private int age;
    private String country;  
    public String getName()
    {
        return name;
    }
    public void setName(String name)
    {
        this.name = name;
    }
    public int getAge()
    {
        return age;
    }
    public void setAge(int age)
    {
        this.age = age;
    }
    public String getCountry()
    {
        return country;
    }
    public void setCountry(String country)
    {
        this.country = country;
    }
}
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        Person obj = new Person();
        obj.setName(sc.nextLine());
        obj.setAge(sc.nextInt());
        obj.setCountry(sc.nextLine());
        System.out.println("Person 1");
        System.out.println("Name: " + obj.getName());
        System.out.println("Age: " + obj.getAge());
        System.out.println("Country: " + obj.getCountry());
    }
}
```





## OUTPUT:

<img width="805" height="450" alt="image" src="https://github.com/user-attachments/assets/d7fdeeff-e9ae-4720-b565-a4ea17b8dfd5" />



## RESULT:
The program successfully creates a Person class with private variables and accesses them using getter and setter methods, demonstrating encapsulation in Java.


