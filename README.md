
0EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
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

#include<stdio.h>
int main(){
    int n;
    scanf("%d",&n);
    
    switch(n){
        case 1:
        printf("one");
        break;
        
        case 2:
        printf("two");
        break;
        
        case 3:
        printf("three");
        break;
        
        case 4:
        printf("four");
        break;
        
        case 5:
        printf("five");
        break;
        
        case 6:
        printf("six");
        break;
        
        case 7:
        printf("seven");
        break;
        
        case 8:
        printf("eigth");
        break;
        
        case 9:
        printf("nine");
        break;
        
        default:
        printf("Greater than 9");
        
    }
}

Output:

![image](https://github.com/user-attachments/assets/6a46fbde-1d67-4dbd-96de-a7ed328821f1)

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

#include<stdio.h>
#include<string.h>

int main(){
    char num[1001];
    int freq[10]={0};
    
    scanf("%s",num);
    
    for(int i=0;i<strlen(num);i++){
        if(num[i]>='0' && num[i]<='9'){
            freq[num[i]-'0']++;
        }
    }
    
    for(int i=0;i<10;i++){
        printf("%d ",freq[i]);
    }
}
Output:

![image](https://github.com/user-attachments/assets/81910212-8672-412b-8f65-07cea1b58fa3)

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

#include <stdio.h>
#include <string.h>
#include <stdbool.h>

// Function to swap two strings
void swap(char arr[][101], int i, int j) {
    char temp[101];
    strcpy(temp, arr[i]);
    strcpy(arr[i], arr[j]);
    strcpy(arr[j], temp);
}

// Function to find the next lexicographical permutation
bool next_permutation(char arr[][101], int n) {
    int i = n - 2;

    // Step 1: Find the rightmost element which is smaller than its next element
    while (i >= 0 && strcmp(arr[i], arr[i + 1]) >= 0) {
        i--;
    }

    if (i < 0) {
        return false;  // No more permutations
    }

    int j = n - 1;
    while (strcmp(arr[j], arr[i]) <= 0) {
        j--;
    }

    // Step 2: Swap elements at i and j
    swap(arr, i, j);

    // Step 3: Reverse the elements after position i
    int left = i + 1, right = n - 1;
    while (left < right) {
        swap(arr, left, right);
        left++;
        right--;
    }

    return true;
}

// Function to print the permutation
void print_permutation(char arr[][101], int n) {
    for (int i = 0; i < n; i++) {
        printf("%s ", arr[i]);
    }
    printf("\n");
}

int main() {
    int n;
    scanf("%d", &n);

    char arr[n][101];  
    for (int i = 0; i < n; i++) {
        scanf("%s", arr[i]);
    }
    print_permutation(arr, n);
    while (next_permutation(arr, n)) {
        print_permutation(arr, n);
    }

    return 0;
}


Output:

![image](https://github.com/user-attachments/assets/b7f10327-06c3-422b-b7af-b18fc455cffb)

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

#include <stdio.h>

int main() {
    int n ;
    scanf("%d",&n);
        int size = 2 * n - 1; 
    for (int i = 0; i < size; i++) {
        for (int j = 0; j < size; j++) {
            
            int min = i < j ? i : j;
            min = min < size - i ? min : size - i - 1;
            min = min < size - j ? min : size - j - 1;

            
            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
Output:

![image](https://github.com/user-attachments/assets/0655f769-f7c4-49e6-a894-98529b8625b4)

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

#include <stdio.h>

int square() {
    int num;
    
    printf("Enter a number: ");
    scanf("%d", &num);

    return num * num; 
}

int main() {
    int result;
    result = square();

    printf("Square of the number is: %d\n", result);

    return 0;
}


Output:

![image](https://github.com/user-attachments/assets/2d5329f9-4b37-4d78-a068-8220200b1bc3)


Result:
Thus, the program is verified successfully
