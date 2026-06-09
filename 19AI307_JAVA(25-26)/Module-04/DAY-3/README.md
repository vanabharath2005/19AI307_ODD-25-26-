# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
To write a Java program demonstrating Composition and Abstract Factory Pattern by creating animal families of different regions and displaying interactions between herbivores and carnivores.



## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Create interfaces Herbivore and Carnivore.
Create concrete animal classes (e.g., Wildebeest, Lion, Deer, Tiger) implementing those interfaces.
Create an abstract factory class for producing families of animals.
Implement region-based factories (AfricaFactory, AsiaFactory).
In the main program, instantiate factories and show interactions.
Print the result.
Stop the program.
```





## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by:  VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Buffalo implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Wildebeest(); }
    public Carnivore createCarnivore() { return new Lion(); }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Buffalo(); }
    public Carnivore createCarnivore() { return new Tiger(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```






## OUTPUT:


<img width="578" height="252" alt="image" src="https://github.com/user-attachments/assets/b92b5b73-68bb-4c30-8df5-c621c079dfea" />


## RESULT:
Thus, the program using Composition and Abstract Factory Pattern was successfully implemented and executed to create animal interactions for African and Asian regions.
