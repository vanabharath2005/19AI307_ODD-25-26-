# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to convert a string to an integer using a wrapper class and perform addition.


## AIM:
To convert string inputs into integers using the wrapper class and perform addition.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Add the two integers.
Display the sum.
```





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String str1 = scanner.next();

        String str2 = scanner.next();

        scanner.close();

        try {
            int num1 = Integer.parseInt(str1);
            int num2 = Integer.parseInt(str2);


            int sum = num1 + num2;
            System.out.println("Sum = " + sum);
        } catch (NumberFormatException e) {
            System.out.println("Invalid input. Please enter a valid number.");
        }
    }
}
```






## OUTPUT:


<img width="447" height="290" alt="image" src="https://github.com/user-attachments/assets/b28cd2ca-ff9f-4a33-b4c6-99224f5b1440" />


## RESULT:
The program successfully converts strings to integers and displays their sum.
