# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program that defines a method cube(int x) which internally calls another method square(int x) to compute the cube of a number using the formula: cube = x * square(x).

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Create a method square(int x) that returns the value of x * x.
Create another method cube(int x) that:
Calls square(x)
Multiplies the result by x
Returns the final cube value.
In the main method:
Read or assign a value for x
Call the cube(x) method
Display the cube.
End the program.

```



## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by:VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```

import java.util.*;
public class Main
{
    static int square(int x)
    {
        return x*x;
    }
    static int cube(int x)
    {
        return x*square(x);
    }
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        System.out.println(cube(n));
    }
}
```





## OUTPUT:

<img width="351" height="110" alt="image" src="https://github.com/user-attachments/assets/352f2bf8-ac0d-4d9e-bf66-8a35db6a4148" />



## RESULT:
The program successfully calculates the cube of a given number by calling the square() method from within the cube() method, demonstrating method calling and reuse in Java.
