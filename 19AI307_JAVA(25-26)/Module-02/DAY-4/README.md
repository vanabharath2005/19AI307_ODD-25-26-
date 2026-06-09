# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a java code to implement a parameterised constructor that will initialize the id,name,age,gender,doj,dob of the student and print the details using user defined function.

## AIM:
To write a Java program that implements a parameterized constructor to initialize the details of a student such as ID, name, age, gender, date of joining (doj), and date of birth (dob), and to print these details using a user-defined function.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Create a class named Student.
Declare instance variables:
id (int)
name (String)
age (int)
gender (String)
doj (date of joining) (String)
dob (date of birth) (String)
Create a parameterized constructor to initialize all the variables.
Create a user-defined function (e.g., displayDetails()) to print the student's information.
In the main method:
Read the student details from the user.
Create an object of Student using the parameterized constructor.
Call the display function to show the student details.
End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
class Student
{
    int id, age;
    String name, gender, doj, dob;
    Student(int id, String name, int age, String gender, String doj, String dob)
    {
        this.id = id;
        this.name = name;
        this.age = age;
        this.gender = gender;
        this.doj = doj;
        this.dob = dob;
    }

    void display()
    {
        System.out.println("--- Student Details ---");
        System.out.println("ID: " + id);
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("Gender: " + gender);
        System.out.println("Date of Joining: " + doj);
        System.out.println("Date of Birth: " + dob);
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int id = sc.nextInt();
        String name = sc.next();
        int age = sc.nextInt();
        String gender = sc.next();
        String doj = sc.next();
        String dob = sc.next();
        Student obj = new Student(id, name, age, gender, doj, dob);
        obj.display();
    }
}
```





## OUTPUT:

<img width="785" height="702" alt="image" src="https://github.com/user-attachments/assets/7a6b3a77-277a-4917-996c-16f46c371dcd" />



## RESULT:
The program successfully initializes student details using a parameterized constructor and prints them using a user-defined function.
