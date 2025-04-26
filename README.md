# Module-8-Lab-Assignment
EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER

Aim:
To write a C program print the lowercase English word corresponding to the number

Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```
#include <stdio.h>

int main() {
    int num;

    printf("Enter a number (70 to 80): ");
    scanf("%d", &num);

    printf("The word is: ");

    switch(num) {
        case 70: printf("seventy"); break;
        case 71: printf("seventy-one"); break;
        case 72: printf("seventy-two"); break;
        case 73: printf("seventy-three"); break;
        case 74: printf("seventy-four"); break;
        case 75: printf("seventy-five"); break;
        case 76: printf("seventy-six"); break;
        case 77: printf("seventy-seven"); break;
        case 78: printf("seventy-eight"); break;
        case 79: printf("seventy-nine"); break;
        case 80: printf("eighty"); break;
        default: printf("invalid number (must be between 70 and 80)");
    }

    printf("\n");
    return 0;
}


```




Output:

![image](https://github.com/user-attachments/assets/ad04cbfa-ca51-46a4-8df2-015774afae2b)


Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .

Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.

Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```

#include <stdio.h>

int main() {
    char a[50];  // Declare char array to store the string
    int c;       // Counter variable to store the frequency of each digit
    int h;       // Variable to loop through each digit from 0 to 3

    // Input a string
    printf("Enter a string: ");
    scanf("%s", a);

    // Outer loop for each digit from 0 to 3
    for (h = 0; h <= 3; h++) {
        c = 0;  // Initialize counter to 0 for each digit
        
        // For each character in the string
        for (int i = 0; a[i] != '\0'; i++) {
            if (a[i] == '0' + h) {  // Check if the character matches the current digit
                c++;  // Increment the counter if there's a match
            }
        }

        // Print the count of the current digit, followed by a space
        printf("%d ", c);
    }

    printf("\n");  // Print newline at the end
    return 0;
}


```



Output:







Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:

//type your code here




Output:


//paste your output here






Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

//type your code here




Output:


//paste your output here






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

//type your code here




Output:


//paste your output here






Result:
Thus, the program is verified successfully



























