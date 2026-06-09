# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.


## AIM:
To write a Java program that reads a string from the user and prints the reversed string using the StringBuilder reverse() method.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Create a Scanner object to read input from the user.
Read the input string using next().
Create a StringBuilder object and pass the input string to it.
Use the reverse() method of StringBuilder to reverse the string.
Print the reversed string.
End the program.
```





## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by:VANA BHARATH D
RegisterNumber: 212223040231
*/
```

## SOURCE CODE:
```
import java.util.*;

class prog{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        String a = sc.next();
        StringBuilder sb = new StringBuilder(a);
        System.out.println("Reversed string: " + sb.reverse());
    }
}
```



## OUTPUT:

<img width="781" height="362" alt="image" src="https://github.com/user-attachments/assets/675f3f0d-409a-4c68-89da-a38e7bacf599" />


## RESULT:
Thus, the Java program to reverse a given string was executed successfully.
