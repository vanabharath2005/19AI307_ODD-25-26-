# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## AIM:
To Write a program to demonstrate chaining of streams (BufferedReader on top of InputStreamReader on top of System.in)

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Create a BufferedReader object chained with InputStreamReader to read input from the keyboard.
Read the user’s name as a string using readLine().
Read the age as a string, then convert it to an integer using Integer.parseInt().
Display the user details (name and age) on the screen.
Close the BufferedReader and handle any possible IOException.
```





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: VANA BHARATH D
RegisterNumber: 212223040231
*/
```

## SOURCE CODE:

```
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;

public class ChainingStreamsExample {
    public static void main(String[] args) {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

        try {
            String name = br.readLine(); 

            String ageInput = br.readLine(); 
            int age = Integer.parseInt(ageInput); 

            System.out.println("--- User Details ---");
            System.out.println("Name: " + name);
            System.out.println("Age: " + age);

            br.close();
        } catch (IOException e) {
            e.printStackTrace();
        }
    }
}
```





## OUTPUT:
<img width="701" height="402" alt="564539199-234259fe-b2de-4385-b85f-cb8c70a525f5" src="https://github.com/user-attachments/assets/e78ab5cd-7ac2-41ed-9774-8686e7319ae9" />



## RESULT:
Thus, the program to demonstrate chaining of streams is executed successfully.
