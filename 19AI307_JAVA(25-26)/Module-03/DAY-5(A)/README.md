# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to calculate the sum of each digit raised to the power of the total number of digits using an inner class. Check whether the given number is an Armstrong number or not.

## AIM:

To write a Java program that checks whether a given number is an Armstrong number by implementing an inner class architecture.
## ALGORITHM :
1. Start the program and initialize a Scanner object to accept a number from the user.

2. Define an outer class ArmstrongDetector containing an inner class named Checker.

3. Implement a method verify(int num) inside the inner class to calculate the Armstrong mathematical logic.

4. Instantiate the inner class in the main method by first creating an instance of the outer class.

5. Call the verify method using the inner class object reference, passing the user-inputted number.

6. Print the final result stating whether the number matches its power-sum matrix and stop.



## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Deepika R
RegisterNumber: 212223230038
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class ArmstrongDetector {
    // Inner class to handle the calculation logic
    class Checker {
        void verify(int num) {
            int temp = num;
            int sum = 0;
            int digits = Integer.toString(num).length();

            while (temp > 0) {
                int digit = temp % 10;
                sum += (int) Math.pow(digit, digits);
                temp /= 10;
            }

            if (sum == num) {
                System.out.println(num + " is an Armstrong number.");
            } else {
                System.out.println(num + " is not an Armstrong number.");
            }
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int num = sc.nextInt();

        // Instantiating the outer class, then the inner class
        ArmstrongDetector outer = new ArmstrongDetector();
        ArmstrongDetector.Checker inner = outer.new Checker();

        // Calling the method from the inner class
        inner.verify(num);
        
        sc.close();
    }
}

```






## OUTPUT:
<img width="705" height="236" alt="image" src="https://github.com/user-attachments/assets/4a4f8fdc-9eb0-43c2-ab6b-8bb68b86696d" />



## RESULT:
Thus the java program to implement inner class was executed successfully.
