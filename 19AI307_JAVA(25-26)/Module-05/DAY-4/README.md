# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a Java program to demonstrate **Thread Priority** by setting and displaying the current thread’s name and priority.

---

## AIM:

To implement the concept of **Thread Priority in Java** by modifying and displaying thread properties such as name and priority.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a class named `Main`.
4. Create a `Scanner` object to read input from the user.
5. Read the thread name from the user.
6. Access the current thread using `Thread.currentThread()`.
7. Set the thread name using `setName()`.
8. Display:

* Thread priority using `getPriority()`
* Thread name using `getName()`
* Full thread details using `toString()`

9. End the program.

---

## PROGRAM:

```java id="v7m2kp"
/*
Program to implement a Thread Priority Concept using Java
Developed by: Deepika R
RegisterNumber: 212223230038
*/
```

## SOURCE CODE:

```java id="r9x4qz"
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();

        t.setName(threadName);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="348" height="142" alt="image" src="https://github.com/user-attachments/assets/a997a53c-1f01-44ec-bc35-88146a9d8c22" />


---

## RESULT:

Thus, the Java program to demonstrate **Thread Priority and thread properties** was implemented successfully and the output was verified.
