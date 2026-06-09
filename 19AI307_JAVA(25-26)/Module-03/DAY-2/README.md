# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program demonstrating method overriding. Create a class Animal with a method sound(). Subclass it as Dog, Cat, Cow, each overriding the sound() method.

## AIM:
To write a Java program that demonstrates method overriding using inheritance and polymorphism.



## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Override the sound() method in each subclass to print specific sounds.
In main(), use an Animal reference to point to each subclass object.
Call the sound() method to demonstrate runtime polymorphism
```





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
 ```
import java.util.Scanner;

class Animal {
    void sound() {
        System.out.println("Unknown animal");
    }
}

class Dog extends Animal {
    @Override
    void sound() {
        System.out.println("Dog barks");
    }
}

class Cat extends Animal {
    @Override
    void sound() {
        System.out.println("Cat meows");
    }
}

class Cow extends Animal {
    @Override
    void sound() {
        System.out.println("Cow moos");
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        while (sc.hasNextLine()) {
            String input = sc.nextLine().trim();
            if (input.isEmpty()) continue;

            Animal a;
            switch(input.toLowerCase()) {
                case "dog": a = new Dog(); break;
                case "cat": a = new Cat(); break;
                case "cow": a = new Cow(); break;
                default: a = new Animal();
            }
            a.sound();
        }
        sc.close();
    }
}
```





## OUTPUT:


<img width="482" height="350" alt="image" src="https://github.com/user-attachments/assets/91ee63cf-169c-4916-8404-c6e810eb0578" />


## RESULT:
The program successfully demonstrates method overriding, showing different behaviors of the sound() method for different animal subclasses.
