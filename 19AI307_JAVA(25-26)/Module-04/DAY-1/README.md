# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
If an Integer object is set to null, and you attempt to call .toString() on it, what happens? How can you prevent your code from throwing an exception in such cases?

## AIM:
To write a Java program that demonstrates how a NullPointerException occurs when accessing methods on a null Integer object, and how to handle it using a try–catch block.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Read an integer value input.
If the input is 0, assign null to the Integer object num; otherwise assign the input value.
Use a try block to call num.toString():
If num is not null, print its string representation.
If num is null, a NullPointerException will be thrown.
Catch the NullPointerException and print "Null Integer".
Close the scanner.
End the program.
```




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class NullPointerIntegerExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int input = sc.nextInt();
        Integer num = (input == 0) ? null : input;

        try {
            System.out.println(num.toString());
        } catch (NullPointerException e) {
            System.out.println("Null Integer");
        }

        sc.close();
    }
}
```






## OUTPUT:


<img width="617" height="355" alt="image" src="https://github.com/user-attachments/assets/87ed7f04-3916-47fb-9ea4-a6cb82ff874f" />


## RESULT:
The program successfully demonstrates how invoking a method on a null Integer object triggers a NullPointerException, and shows how the exception can be caught and handled gracefully by printing "Null Integer"
