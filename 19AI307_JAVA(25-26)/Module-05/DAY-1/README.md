# Ex.No:5(A) INPUTSTREAMREADER

## QUESTION:

Write a Java program to demonstrate file handling using `FileWriter` by creating a file and writing content into it.

---

## AIM:

To implement file handling in Java using `FileWriter` for creating a file and writing data into it.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary packages:

* `java.io.FileWriter`
* `java.io.IOException`
* `java.util.Scanner`

3. Create a class named `CreateFile`.
4. In the `main()` method:

* Create a `Scanner` object to read input from the user.
* Read the file name.
* Read the content to be written into the file.

5. Use a `try` block to:

* Create a `FileWriter` object with the given file name.
* Write the content into the file using `write()`.
* Close the file using `close()`.
* Display success messages.

6. Use a `catch` block to handle `IOException`.
7. Display an error message if an exception occurs.
8. Use the `finally` block to close the scanner.
9. End the program.

---

## PROGRAM:

```java id="k8x5mr"
/*
Program to implement a InputStreamReader using Java
Developed by: Deepika R
RegisterNumber: 212223230038
*/
```

## SOURCE CODE:

```java id="q4m9zt"
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class CreateFile{

    public static void main(String[] ar){

        Scanner s = new Scanner(System.in);

        String fileName = s.nextLine();

        String content = s.nextLine();

        try{

            FileWriter writer = new FileWriter(fileName);

            writer.write(content);

            writer.close();

            System.out.println("File created: " + fileName);

            System.out.println("Content written to the file successfully.");

        }catch(IOException e){

            System.out.println("An error occurred.");

            e.printStackTrace();

        }finally{

            s.close();
        }
    }
}
```

---

## OUTPUT:

<img width="507" height="137" alt="image" src="https://github.com/user-attachments/assets/90434ac1-9f8c-41f4-ba8a-c0c0c3fc1e81" />

---

## RESULT:

Thus, the Java program to demonstrate file handling using `FileWriter` was implemented successfully and the output was verified.
