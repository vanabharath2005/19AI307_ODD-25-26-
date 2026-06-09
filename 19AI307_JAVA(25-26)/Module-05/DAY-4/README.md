# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

## AIM:
To Write a java program for determine the priority and name of the current thread.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Read a thread name from the user using Scanner.
Get the reference of the current running thread using Thread.currentThread().
Change the name of the current thread to the user-provided name.
Retrieve the current thread’s priority using getPriority().
Print the thread’s priority, updated name, and full thread information.
```





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class CurrentThreadInfo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread currentThread = Thread.currentThread();

        currentThread.setName(threadName);

        int priority = currentThread.getPriority();

        System.out.println("Priority of Thread: " + priority);
        System.out.println("Name of Thread: " + currentThread.getName());
        System.out.println(currentThread);

        sc.close();
    }
}
```






## OUTPUT:
<img width="810" height="216" alt="564540446-b2db9cf1-77ce-4451-bc07-0b07bbc50590" src="https://github.com/user-attachments/assets/8db2db00-a573-4eb1-9524-9ff5fa90dda1" />



## RESULT:
Thus, the program to determine the priority and name of the current thread is executed successfully.
