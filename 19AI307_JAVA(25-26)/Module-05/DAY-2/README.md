# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION

## QUESTION:

Write a Java program to demonstrate **Serialization and Deserialization** using `DataOutputStream` and `DataInputStream` for writing and reading UTF strings from a file.

---

## AIM:

To implement **Serialization and Deserialization** in Java using file streams to store and retrieve data from a file.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary packages:

* `java.io.*`
* `java.util.Scanner`

3. Create a class named `DataInputStreamUTFExample`.
4. In the `main()` method:

* Declare the file name.
* Create a `Scanner` object to read input from the user.

5. Read a string input from the user.
6. Use a `try` block to:

* Create a `DataOutputStream` object.
* Write the string into the file using `writeUTF()`.
* Close the output stream.

7. Create a `DataInputStream` object.
8. Read the string from the file using `readUTF()`.
9. Display the retrieved string.
10. Close the input stream.
11. Handle exceptions using `catch(IOException e)`.
12. End the program.

---

## PROGRAM:

```java id="t9m4zp"
/*
Program to implement a Serialization and Deserialization using Java
Developed by: Deepika R
RegisterNumber: 212223230038
*/
```

## SOURCE CODE:

```java id="f6x2qn"
import java.io.*;
import java.util.Scanner;

public class DataInputStreamUTFExample {

    public static void main(String[] args) {

        String fileName = "utfdata.dat";

        Scanner s = new Scanner(System.in);

        String input = s.nextLine();

        try{

            DataOutputStream dos =
            new DataOutputStream(
            new FileOutputStream(fileName));

            dos.writeUTF(input);

            dos.close();

            DataInputStream dis =
            new DataInputStream(
            new FileInputStream(fileName));

            String str = dis.readUTF();

            dis.close();

            System.out.println("String read from file: " + str);

        }catch(IOException e){

            System.out.println("Error occurred while processing the file.");
        }

        s.close();
    }
}
```

---

## OUTPUT:

<img width="393" height="116" alt="image" src="https://github.com/user-attachments/assets/4bdfc8d5-958c-4991-a3de-077139532fc3" />


---

## RESULT:

Thus, the Java program to demonstrate **Serialization and Deserialization** using `DataOutputStream` and `DataInputStream` was implemented successfully and the output was verified.
