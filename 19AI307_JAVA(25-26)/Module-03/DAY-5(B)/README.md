# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program that checks whether a given number is an Armstrong number by calculating the sum of its digits raised to the power of the total digit count using Math.pow() and the Integer wrapper class.


## ALGORITHM :

1. Start the program and initialize a Scanner object to capture user input.

2. Read an integer number from the user and store it in a variable named num.

3. Determine the total number of digits by converting num to a string using the wrapper class method Integer.toString(num).length().

4. Extract each digit sequentially using a loop with the modulus operator (%) and divide the number by 10 (/) in each iteration.

5. Compute the power of each extracted digit using Math.pow(digit, digits) and add it to a running total sum.

6. Compare the final sum with the original number, print the corresponding Armstrong matching result message, and stop.



## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Deepika R
RegisterNumber:  212223230038
*/
```

## SOURCE CODE:

```import java.util.*;
class prog{
    public static void main(String[] args){
        Scanner sc=new Scanner(System.in);
        int num=sc.nextInt();
        int temp=num;
        int sum=0;
        int digits=Integer.toString(num).length();
        while(temp>0){
            int digit=temp%10;
            sum+=(int)Math.pow(digit,digits);
            temp/=10;
        }
        if(sum==num){
            System.out.println(num + " is an Armstrong number.");
        }
        else{
            System.out.println(num+ " is not an Armstrong number.");
        }
    }
}
```





## OUTPUT:

<img width="688" height="228" alt="image" src="https://github.com/user-attachments/assets/533c5626-dd54-4c32-929d-57335cf91746" />


## RESULT:
Thus the program to implement wrapper class for the given input was exeecuted successfully.
