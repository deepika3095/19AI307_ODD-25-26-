# Ex.No:5(E) MULTITHREADING – SYNCHRONIZATION

## QUESTION:

Write a Java program to demonstrate **Multithreading using ExecutorService** where multiple tasks compute the square of numbers concurrently.

---

## AIM:

To implement **multithreading in Java using ExecutorService** and understand concurrent execution of tasks.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary packages:

* `java.util`
* `java.util.concurrent.ExecutorService`
* `java.util.concurrent.Executors`
* `java.util.concurrent.TimeUnit`

3. Create a class `SquareTask` implementing `Runnable`.
4. Store an integer number in the class.
5. Override the `run()` method to compute and display the square of the number.
6. In the `main()` method:

* Read the number of tasks `n`.
* Create a thread pool using `Executors.newFixedThreadPool(2)`.

7. Use a loop to:

* Read each number.
* Submit each task to the thread pool.

8. Shut down the executor service using `shutdown()`.
9. Wait for all tasks to complete using `awaitTermination()`.
10. End the program.

---

## PROGRAM:

```java id="x5m9qk"
/*
Program to implement a Synchronization concept using Java
Developed by: Deepika R
RegisterNumber: 212223230038
*/
```

## SOURCE CODE:

```java id="p8v4tz"
import java.util.Scanner;
import java.util.concurrent.ExecutorService;
import java.util.concurrent.Executors;
import java.util.concurrent.TimeUnit;

class SquareTask implements Runnable {

    int number;

    SquareTask(int number) {

        this.number = number;
    }

    public void run() {

        System.out.println("Square: " + (number * number));
    }
}

public class Main {

    public static void main(String[] args) throws InterruptedException {

        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        ExecutorService pool = Executors.newFixedThreadPool(2);

        for (int i = 0; i < n; i++) {

            int num = sc.nextInt();

            pool.submit(new SquareTask(num));
        }

        pool.shutdown();

        pool.awaitTermination(1, TimeUnit.MINUTES);

        sc.close();
    }
}
```

---

## OUTPUT:

<img width="207" height="143" alt="image" src="https://github.com/user-attachments/assets/550c52e8-b11b-4038-8f7b-0470e531bff2" />


---

## RESULT:

Thus, the Java program to demonstrate **Multithreading using ExecutorService** was implemented successfully and the output was verified.
