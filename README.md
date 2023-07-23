# Replace-All-0-s-With-1-In-A-Given-Integer-C-Program
Program to Replace all 0’s with 1 in a given integer
Here we will discuss how to replace all the 0’s with 1 in a given integer using C programming language.

The concept is simple, find the digits of the integer. Compare each digit with 0 if the digit is equal to 0 then replace it with 1. Construct the new integer with the replaced digits.

Thrashing in Operating System
While loop in C
The program for Implement a C Program to replace all 0’s with 1 in a given integer as an input, all the 0’s in the number has to be replaced with 1.

Question can come like Way 1
Write a code to change all zero's as one's (0s as 1s) in a given number? ex: 120014 needs to be printed as 121114
Question can come like Way 2
implement a c program to replace all 0's with 1 in a given integer as an input, all the 0's in the number has to be replaced with 1.
Algorithm
Take Input in num and initialize a variable num with with value 0
If num is equals to zero then update the value of num2 to 1
Iterate using a while loop until num is greater then 0
For each iteration initialize a variable rem and store unit digit of num
If rem equals to 0 then set rem to 1
Set num to num divide by 10 & num2 equals to num2*10+rem
Reverse and print num2
Replace all 0's with 1 in C
C code
Run
#include<stdio.h>

    //main program

    int main()

    {

        int num,num2=0;

        printf("Enter number: ");

        //user input

        scanf("%d", &num);

        //checking for 0 input

        if(num == 0)

            num2=1;

        //converting 0 to 1

        while(num>0)

        {

            int rem = num%10;

            if(rem == 0)

                rem = 1;

            num = num/10;

            num2=num2*10+rem;

        }

       num = 0 ; // Store the reverse of num2

       while(num2>0){

        int r = num2%10;

        num= num*10 + r;

        num2 /= 10;

      }

        //converted number

        printf("Converted number is: %d" ,num);

        return 0;

    }
Output
Enter number: 900120678
Converted number is: 911121678
