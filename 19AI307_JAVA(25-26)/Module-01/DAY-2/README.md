# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
```
A dragon wakes based on temperature:

If temperature < 0, it hibernates. If 0 ≤ temp ≤ 20, it snoozes. If 21 ≤ temp ≤ 35, it wakes. If temp > 35, it gets angry.

Write a java program to get the user input for temperature and display appropriate output.

Example Input: -5

Result : Hibernating
```


## AIM:
To write a java program to get the user input for temperature and display appropriate output.

## ALGORITHM :
1.Start the program. 2.Import the necessary package 'java.util' 3.Create a Scanner object to read input from the user. 4.Read an integer value and store it in the variable temp. 5.Check if temp < 0 : If true, print "Hibernating". 6.Else if temp is between 0 and 20 (inclusive) : Print "Snoozing". 7.Else if temp is between 21 and 35 (inclusive): Print "Awake". 8.Else (i.e., temp > 35): Print "Angry".





## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Sri Hari R 
RegisterNumber: 212223043202
*/
```

## SOURCE CODE:
```
import java.util.*;

class prog{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int t=sc.nextInt();
        if (t<0)
        {
            System.out.println("Hibernating");
        }
        else if(t>=0 && t<=20)
        {
            System.out.println("Snoozing");
        }
        else if (t>=21 && t<=35)
        {
            System.out.println("Awake");
        }
        else
        {
            System.out.println("Angry");
        }
    }
}   
```






## OUTPUT:
<img width="472" height="368" alt="image" src="https://github.com/user-attachments/assets/9a8c09c8-fe3a-43a6-9bf3-cb67223d0d6d" />



## RESULT:
Thus, a java program to get the user input for temperature and display appropriate output is executed successfully.
     
