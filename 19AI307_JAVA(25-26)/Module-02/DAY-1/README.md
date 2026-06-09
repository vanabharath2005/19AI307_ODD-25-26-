# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Teacher with attributes: name (String), subject (String), and experience (int, years).

## AIM:


## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Define a class Teacher with the following attributes:name (String),subject (String),experience (int,years)
Create a constructor to initialize these attributes.
Create an object of the Teacher class in the main method.
Display the teacher’s details using print statements.
End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: VANA BHARATH D 
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:

```
import java.util.*;
class Teacher
{
    String name;
    String subject;
    int experience;  
    void print()
    {
        System.out.println("Mr. " + name + " teaches " + subject + " and has " + experience + " years experience.");
    }
}
public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        Teacher obj = new Teacher();
        obj.name = sc.nextLine();
        obj.subject = sc.nextLine();
        obj.experience = sc.nextInt();
        obj.print();
    }
}
```





## OUTPUT:
<img width="856" height="215" alt="image" src="https://github.com/user-attachments/assets/f2e304a1-50de-4bf6-9ab9-4e18c5d33e9b" />



## RESULT:
The program successfully defines a Teacher class with attributes for name, subject, and experience, creates an object with the given values, and displays the teacher’s details correctly.
