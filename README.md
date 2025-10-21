# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>
#include <math.h>

void calculateEMI(float principal, float annualRate, int tenureMonths) {
    float monthlyRate = annualRate / (12 * 100);
    float emi = (principal * monthlyRate * pow(1 + monthlyRate, tenureMonths)) /
                (pow(1 + monthlyRate, tenureMonths) - 1);
    printf("EMI for loan amount %.2f at %.2f%% for %d months is: %.2f\n",
           principal, annualRate, tenureMonths, emi);
}

int main() {
    float p, r;
    int n;
    scanf("%f %f %d", &p, &r, &n);
    calculateEMI(p, r, n);
    return 0;
}


## OUTPUT
100000 8.5 36

EMI for loan amount 100000.00 at 8.50% for 36 months is: 3151.93



## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
Write a C program to generate Fibonacci series
## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
#include <stdio.h>

void generateFibonacci(int terms) {
    int a = 0, b = 1, next, i;
    for (i = 0; i < terms; i++) {
        printf("%d ", a);
        next = a + b;
        a = b;
        b = next;
    }
    printf("\n");
}

int main() {
    int n;
    scanf("%d", &n);
    generateFibonacci(n);
    return 0;
}

## OUTPUT
7
0 1 1 2 3 5 8






## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, i;
    scanf("%d", &n);
    int a[n];
    for (i = 0; i < n; i++)
        scanf("%d", &a[i]);
    printf("%d\n", a[n - 1]);
    return 0;
}

## OUTPUT
5
10 20 30 40 50
50







## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
#include <stdio.h>

int main() {
    int n, i, count = 0;
    scanf("%d", &n);
    int a[n];
    for (i = 0; i < n; i++) {
        scanf("%d", &a[i]);
        if (a[i] > 0)
            count++;
    }
    printf("%d\n", count);
    return 0;
}

## OUTPUT
6
-3 7 0 4 -1 9
3



## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.





 
 


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
#include <stdio.h>

int main() {
    int n, i;
    scanf("%d", &n);
    int a[n];
    for (i = 0; i < n; i++)
        scanf("%d", &a[i]);
    for (i = 0; i < n; i++) {
        if (a[i] % 2 == 0)
            printf("E ");
        else
            printf("%d ", a[i]);
    }
    printf("\n");
    return 0;
}

## Output:
6
4 7 2 9 10 3 
E 7 E 9 E 3

## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



