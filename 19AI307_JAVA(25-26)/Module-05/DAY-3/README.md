# Ex.No:5(C) FILE HANDLING USING JAVA

## QUESTION:

Write a Java program to read multiple lines of input and display only those lines that contain the word **"Java"**, until the user enters `"exit"`.

---

## AIM:

To implement **file handling concepts in Java using input processing**, where specific content (lines containing a keyword) is filtered and displayed.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Main`.
4. Create a `Scanner` object to read input from the user.
5. Display a message indicating filtering of lines containing the word `"Java"`.
6. Start an infinite loop.
7. Read input line by line from the user.
8. Check if the input line equals `"exit"`:

* If yes, terminate the loop.

9. Check if the line contains the word `"Java"`:

* If yes, print the line.

10. Close the scanner.
11. End the program.

---

## PROGRAM:

```java id="c5m8tr"
/*
Program to implement a File Handling using Java
Developed by: Deepika R
RegisterNumber: 212223230038
*/
```

## SOURCE CODE:

```java id="p8v2xq"
import java.util.Scanner;

public class Main{

    public static void main(String[] ar){

        Scanner s = new Scanner(System.in);

        System.out.println("Lines containing the word 'Java':");

        while(true){

            String line = s.nextLine();

            if(line.equals("exit"))
                break;

            if(line.contains("Java"))
                System.out.println(line);
        }

        s.close();
    }
}
```

---

## OUTPUT:

<img width="473" height="145" alt="image" src="https://github.com/user-attachments/assets/22e63d8f-4108-4337-8b39-0d6cefd5b282" />


---

## RESULT:

Thus, the Java program to filter and display lines containing the word **"Java"** was implemented successfully and the output was verified.
