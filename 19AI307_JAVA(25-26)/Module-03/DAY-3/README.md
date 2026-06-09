# Ex.No:3(C) ABSTRACTION

## QUESTION:
Description: Create abstract class GameScore with method finalScore(). Subclasses:

ArcadeGame: score = baseScore + (level × 100)

PuzzleGame: score = (attempts ≤ 3) ? 1000 - (attempts × 100) : 500

Input Format:

First line: 1 or 2 Second line: base, level (or attempts)

Output Format:

Final score (int)

## AIM:
To write a Java program using an abstract class GameScore with subclasses ArcadeGame and PuzzleGame, each implementing its own finalScore() method.

## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Define subclass PuzzleGame where
If attempts ≤ 3, score = 1000 - (attempts × 100)
Else score = 500.
Take user input for game type and relevant values.
Display the final score based on game type.
```



## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: VANA BHARATH D
RegisterNumber: 212223040231
*/
```

## SOURCE CODE:

```
import java.util.*;

abstract class GameScore {
    abstract int finalScore();
}

class ArcadeGame extends GameScore {
    int base, level;
    ArcadeGame(int base, int level) {
        this.base = base;
        this.level = level;
    }
    int finalScore() {
        return base + (level * 100);
    }
}

class PuzzleGame extends GameScore {
    int attempts;
    PuzzleGame(int attempts) {
        this.attempts = attempts;
    }
    int finalScore() {
        if (attempts <= 3)
            return 1000 - (attempts * 100);
        else
            return 500;
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();
        if (type == 1) {
            int base = sc.nextInt();
            int level = sc.nextInt();
            ArcadeGame game = new ArcadeGame(base, level);
            System.out.println(game.finalScore());
        } else if (type == 2) {
            int attempts = sc.nextInt();
            PuzzleGame game = new PuzzleGame(attempts);
            System.out.println(game.finalScore());
        }
    }
}
```





## OUTPUT:

<img width="397" height="286" alt="image" src="https://github.com/user-attachments/assets/ac225f82-4617-47dd-876f-63a7d43d504e" />



## RESULT:
The program successfully demonstrates abstraction and inheritance by computing the final score for different game types using subclass-specific logic.
