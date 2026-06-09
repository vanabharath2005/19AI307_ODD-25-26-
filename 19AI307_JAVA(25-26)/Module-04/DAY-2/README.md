# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.

Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state.

Input Format:

n [Player1] [Player2] ... First line: Integer n – number of players turning on consoles

Next n lines: Each line contains the player's name.

Output Format: For each player, print:

[PlayerName] accessed Master Power Switch. Total accesses so far: [count]

<img width="836" height="337" alt="image" src="https://github.com/user-attachments/assets/b79b01f3-ccdd-4e23-b129-47db630a99ca" />


## AIM:
To implement a Singleton master power switch that logs shared access counts whenever players turn on their consoles.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Read an integer n representing the number of players.
For each of the n players: a. Read the player’s name. b. Access the singleton instance of MasterPowerSwitch using getInstance(). c. Call logAccess() on the instance to increment and retrieve the total access count. d. Print the message: [PlayerName] accessed Master Power Switch. Total accesses so far: [count].
End the program.

```




## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: VANA BHARATH D 
RegisterNumber: 212223040231 
*/
```

## SOURCE CODE:

```
import java.util.*;

class MasterPowerSwitch {
    private static MasterPowerSwitch instance;
    private int accessCount = 0;

    private MasterPowerSwitch() {}

    public static MasterPowerSwitch getInstance() {
        if (instance == null) {
            instance = new MasterPowerSwitch();
        }
        return instance;
    }

    public int logAccess() {
        accessCount++;
        return accessCount;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}
```





## OUTPUT:

<img width="838" height="181" alt="image" src="https://github.com/user-attachments/assets/7fe2b0b9-4a28-44bf-95d4-30cac6956ca6" />



## RESULT:
The program ensures a single shared instance, incrementing and displaying the total access count for each player
