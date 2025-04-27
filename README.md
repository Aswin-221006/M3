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

// Step 3: Function to calculate EMI
void calculateEMI(float principal, float rate, int months) {
    // Convert annual interest rate to monthly interest rate
    float r = rate / 12 / 100;

    // Calculate EMI using the formula
    float emi = (principal * r * pow(1 + r, months)) / (pow(1 + r, months) - 1);

    // Step 5: Display the EMI result
    printf("The EMI is: %.2f\n", emi);
}

int main() {
    float principal, rate;
    int months;

    // Step 2: Read principal amount, rate of interest, and months
    printf("Enter the principal amount: ");
    scanf("%f", &principal);

    printf("Enter the annual rate of interest (in %%): ");
    scanf("%f", &rate);

    printf("Enter the number of months: ");
    scanf("%d", &months);

    // Step 3: Pass values to the function
    calculateEMI(principal, rate, months);

    return 0;
}


## OUTPUT
Enter the principal amount: 500000
Enter the annual rate of interest (in %): 12
Enter the number of months: 24
The EMI is: 25898.45





## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 


# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

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

int main() {
    int n = 6;  // Number of terms for Fibonacci series
    int first = 0, second = 1, next;

    // Step 2: Display the first two terms
    printf("Fibonacci Series for %d terms: \n", n);
    printf("%d %d ", first, second);

    // Step 3 and 4: Add the previous two terms to get the next term
    for (int i = 3; i <= n; i++) {
        next = first + second;  // Add the previous two terms
        printf("%d ", next);     // Display the next term
        first = second;         // Move second to first
        second = next;          // Move next to second
    }

    printf("\n");
    return 0;
}

## OUTPUT
Fibonacci Series for 6 terms:
0 1 1 2 3 5








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
    int n;

    // Step 2: Read the number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];  // Declare an array of size n

    // Step 3: Read the array values
    printf("Enter the elements of the array: \n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Step 4: Print the last element
    printf("The last element of the array is: %d\n", arr[n - 1]);

    return 0;
}

## OUTPUT
Enter the number of elements: 5
Enter the elements of the array:
10 20 30 40 50
The last element of the array is: 50









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
    int n, count = 0;

    // Step 2: Read the number of elements
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];  // Declare an array of size n

    // Step 3: Read the array values
    printf("Enter the elements of the array: \n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Step 4: Count the positive elements
    for (int i = 0; i < n; i++) {
        if (arr[i] > 0) {
            count++;  // Increment count if the element is positive
        }
    }

    // Step 5: Display the result
    printf("Total number of positive elements: %d\n", count);

    return 0;
}


## OUTPUT
Enter the number of elements: 5
Enter the elements of the array:
-1 2 3 -4 5
Total number of positive elements: 3





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
    int n;

    // Step 1: Read the size of the array
    printf("Enter the number of elements in the array: ");
    scanf("%d", &n);

    // Declare the array of integers
    int arr[n];

    // Step 1: Input the elements of the array
    printf("Enter the elements of the array:\n");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }

    // Step 2: Iterate through the array and replace even elements with 'E'
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {  // Check if the element is even
            arr[i] = 'E';  // Replace even element with 'E'
        }
    }

    // Step 4: Output the updated array
    printf("Updated array after replacing even elements with 'E':\n");
    for (int i = 0; i < n; i++) {
        if (arr[i] == 'E') {
            printf("'E' ");
        } else {
            printf("%d ", arr[i]);
        }
    }

    printf("\n");

    return 0;
}

## Output:
 Enter the number of elements in the array: 5
Enter the elements of the array:
1 2 3 4 5
Updated array after replacing even elements with 'E':
1 'E' 3 'E' 5



## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



