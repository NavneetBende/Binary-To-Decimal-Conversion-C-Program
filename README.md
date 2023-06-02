# Binary-To-Decimal-Conversion-C-Program

Binary to Decimal in C
Let’s look at Binary to Decimal in C, we will discuss the C program for binary to decimal conversion. A decimal number can be attained by multiplying every digit of binary digit with a power of 2 and adding each multiplication outcome. The power of the integer starts from 0 and counts to n-1 where n is assumed as the overall digits of integers in binary numbers.

Ex:-  (10110)2 = 
1 * 24 + 0 * 23 + 1 * 22 + 1 * 21 + 0 * 20
16 + 0 + 4 + 2 + 0 = (22)10
Program for Binary to Decimal in C
Working:-
Binary to Decimal in C

For user input num

Initialize i = 0, decimal = 0
Extract the last digit (digit = num% 10)
Calculate decimal equivalent of this digit
Add it to decimal variable
decimal += digit * pow(2,i);
Reduce the number (num /= 10
increment i value

While loop in C
C Program to convert Binary to Decimal Number:
Code
Run
// C Program to convert binary to decimal
#include<stdio.h>
#include<math.h>

// function to convert binary to decimal
int convert(long long num)
{
    int i = 0, decimal= 0;
    
    //converting binary to decimal
    while (num!=0)
    {
        int digit = num % 10;
        decimal += digit * pow(2,i);

        num /= 10;
        i++;
    }
    return decimal;
}

// main program
int main()
{
    // long used rather than int to store large values
    // Ex : int wont store 111111111111 (12 digits) as
    // limit for int is 2147483647 (10 digits)
    long long binary;
    
    printf("Enter binary number: ");
    scanf("%lld", &binary);
    
    printf("%lld", convert(binary));
    
    return 0;
}
Output
Enter binary number: 101
5
While loop in C
Related Pages
Program to Find LCM

Program to find GCD

Program for octal to decimal conversion

Program for hexadecimal to decimal conversion

Program for decimal to binary conversion

Program for Decimal to Binary
Let us look at the program and how to convert manually the same below –

Conversion 2
conversion new
Code Decimal to Binary
Run
#include<stdio.h>


void getBinary(int dec)
{
    // since, we may need to store large binary values using long long
    long long binary = 0;
    int rem, i = 1;
    
    while(dec != 0)
    {
        rem = dec % 2;
        dec /= 2;
        binary += rem * i;
        
        // moving to next position ex: units -> tens
        i *= 10;
    }
    printf("%lld",binary);
}
 
int main()
{
    int dec = 19;
    getBinary(dec);
    return 0;
}
Output
10011
