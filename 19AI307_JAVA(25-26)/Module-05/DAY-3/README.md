# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of words in a file.

## AIM:
To Write a program to count the number of words in a file.
## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Read a full line of text from the user and write it into a file using BufferedWriter.
Open the same file using BufferedReader to read its contents line by line.
For each line, trim it and split it into words using whitespace as the delimiter.
Count all valid words and accumulate the total word count.
Print the total number of words and close all streams properly.
```





## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by:VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.Scanner;

public class WordCountFile {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String fileName = "input.txt";

        try {
            String input = sc.nextLine();

            BufferedWriter writer = new BufferedWriter(new FileWriter(fileName));
            writer.write(input);
            writer.close();

            BufferedReader reader = new BufferedReader(new FileReader(fileName));
            int wordCount = 0;
            String line;
            while ((line = reader.readLine()) != null) {
                String[] words = line.trim().split("\\s+"); 
                if (!line.trim().isEmpty()) {
                    wordCount += words.length;
                }
            }
            reader.close();

            System.out.println("Number of words in the file: " + wordCount);

        } catch (IOException e) {
            e.printStackTrace();
        } finally {
            sc.close();
        }
    }
}
```






## OUTPUT:
<img width="1137" height="250" alt="564540002-464a8ea0-58a3-4297-a4a1-57645ed42f12" src="https://github.com/user-attachments/assets/d9d58e57-4c2f-48fb-9679-36f2d1e35fa1" />



## RESULT:
Thus, the program to count the number of words in a file executed successfully.
