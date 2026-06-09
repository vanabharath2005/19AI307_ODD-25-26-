# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to sort an array in ascending order.

<img width="197" height="252" alt="image" src="https://github.com/user-attachments/assets/1f5687ca-fe37-4a61-b6c8-fb791f5c0728" />


## AIM:
To write a Java program that reads an array of integers and sorts the elements in ascending order using built-in array methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'






## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: VANA BHARATH D
RegisterNumber: 212223040231
*/
```

## SOURCE CODE:
```
import java.util.*;
class prog{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int a[]=new int[n];
        for (int i=0;i<n;i++)
        {
            int x=sc.nextInt();
            a[i]=x;
        }
        Arrays.sort(a);
        for (int i=0;i<n;i++)
        {
            System.out.print(a[i]+ " ");
        }
    }
}
```






## OUTPUT:
<img width="625" height="865" alt="image" src="https://github.com/user-attachments/assets/0a004deb-5e7c-489a-9cf5-2fab187319a8" />



## RESULT:
Thus, the Java program to sort an array in ascending order was executed successfully.
