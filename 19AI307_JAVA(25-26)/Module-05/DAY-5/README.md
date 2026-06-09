# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Read N numbers from user, use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2. Return results in order.

## AIM:
To Read N numbers from user, use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2. Return results in order.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Read T and then read T numbers from the user and store them in a list.
Create a fixed thread pool with 3 threads using Executors.newFixedThreadPool(3).
For each number, submit a task to the executor that returns the number multiplied by 2.
Store all submitted tasks as Future objects and later retrieve their results using future.get().
Print each processed result and finally shut down the executor service.
```





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: VANA BHARATH D
RegisterNumber: 212223040231
*/
```

## SOURCE CODE:

```
import java.util.*;
import java.util.concurrent.*;

public class FixedThreadPoolExample {
    public static void main(String[] args) throws InterruptedException, ExecutionException {
        Scanner sc = new Scanner(System.in);

        int T = Integer.parseInt(sc.nextLine());
        List<Integer> numbers = new ArrayList<>();

        for (int i = 0; i < T; i++) {
            numbers.add(Integer.parseInt(sc.nextLine()));
        }

        ExecutorService executor = Executors.newFixedThreadPool(3);

        List<Future<Integer>> futures = new ArrayList<>();

        for (int num : numbers) {
            Future<Integer> future = executor.submit(() -> num * 2);
            futures.add(future);
        }

        for (Future<Integer> future : futures) {
            System.out.println("Result: " + future.get());
        }

        executor.shutdown();
        sc.close();
    }
}
```





## OUTPUT:
<img width="436" height="450" alt="564540764-8e9741e9-ddb5-40e6-9723-7ef79525545b" src="https://github.com/user-attachments/assets/140fe1af-0f67-4853-98e1-7d4c3f2751ae" />



## RESULT:
Thus, the program to Read N numbers from user, use a fixed thread pool (size 3) to compute the sum of each number multiplied by 2 executed successfully.
