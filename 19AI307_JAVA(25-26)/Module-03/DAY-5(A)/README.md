# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.

## AIM:
To demonstrate accessing an inner class from an outer class in Java

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
In main(), create an object of the outer class.
Use it to create an object of the inner class.
Call the inner class method.
```




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: VANA BHARATH D
RegisterNumber: 212223040231
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class OuterClass {
    String name;

    OuterClass(String name) {
        this.name = name;
    }

    void display() {
        InnerClass inner = new InnerClass();
        inner.showMessage();
    }

    class InnerClass {
        void showMessage() {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("");
        String input = scanner.next();
        scanner.close();

        OuterClass outer = new OuterClass(input);
        outer.display();
    }
}
```






## OUTPUT:

<img width="787" height="241" alt="image" src="https://github.com/user-attachments/assets/3d7f718f-18ca-456c-8237-01fe7a77df9d" />
## RESULT:
The program successfully accesses and prints data from the inner class using the outer class.



