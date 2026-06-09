# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList) into a file.


## AIM:
To Write a Java program to serialize a collection of objects (like ArrayList) into a file.


## ALGORITHM :
```
Start the program.
Import the necessary package 'java.util'
Start by reading the number of students and their details (id, name, marks) from the user and store each entry as a Student object in a list.
Serialize (save) the list of Student objects into a file using ObjectOutputStream.
Deserialize (load) the list back from the file using ObjectInputStream.
Retrieve the list of Student objects from the file and print each student's details.
Handle exceptions such as IOException and ClassNotFoundException to avoid runtime errors.
```




## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: VANA BHARATH D
RegisterNumber:  212223040231
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

class Student implements Serializable {
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput {

    public static void serializeStudents(List<Student> students, String fileName) {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } catch (IOException e) {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } catch (IOException | ClassNotFoundException e) {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); 
        for (int i = 0; i < n; i++) {
            int id = Integer.parseInt(scanner.nextLine());
            String name = scanner.nextLine();
            double marks = Double.parseDouble(scanner.nextLine());
            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);

        if (deserializedStudents != null) {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```






## OUTPUT:

<img width="1217" height="390" alt="564539577-b503c48d-034d-4cc3-8723-e601c571813f" src="https://github.com/user-attachments/assets/f662b856-6ac7-47f8-85fe-ddae6987c945" />


## RESULT:
Thus, the program to serialize a collection of objects (like ArrayList) into a file executed successfully.

