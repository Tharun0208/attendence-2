# attendence-2
## 1. Write a C program to traverse a 2D matrix and print the values until a negative number is found. Use break statement.

```
#include <stdio.h>

int main() {
    int rows, cols;
    
 
    printf("Enter number of rows and columns: ");
    scanf("%d %d", &rows, &cols);

    int matrix[rows][cols];

    printf("Enter matrix elements:\n");
    for(int i = 0; i < rows; i++) {
        for(int j = 0; j < cols; j++) {
            scanf("%d", &matrix[i][cols]);
        }
    }

    printf("Matrix traversal until negative number:\n");

 
    for(int i = 0; i < rows; i++) {
        for(int j = 0; j < cols; j++) {
            if(matrix[i][j] < 0) {
                break;
            }
            printf("%d ", matrix[i][j]);
        }
        printf("\n");
    }

    return 0;
}
```
## output
<img width="570" height="782" alt="image" src="https://github.com/user-attachments/assets/120f6905-aff1-4ed9-a894-ebb8ca7530d2" />

## 2. Write a C program to print the numbers from 1 to 100 but avoid printing multiples of 3 and number containing digit 5(5,15,25,35,..). Use continue in the program.
```
#include <stdio.h>

int main() {
    for(int i = 1; i <= 100; i++) {

     
        if(i % 3 == 0) {
            continue;
        }

        int temp = i;
        int hasFive = 0;

        while(temp > 0) {
            if(temp % 10 == 5) {
                hasFive = 1;
                break;
            }
            temp /= 10;
        }

        if(hasFive) {
            continue;
        }

        printf("%d ", i);
    }

    return 0;
}
```
## output
<img width="826" height="454" alt="image" src="https://github.com/user-attachments/assets/f686f611-4328-4699-b891-8155418dbaee" />

## 3. Write a C program that performs division of two user inputs and uses goto  to handle errors like division by zero or invalid input by redirecting control for re-entry.

```
#include <stdio.h>

int main() {
    float num1, num2;

start:  

    printf("Enter two numbers: ");

   
    if (scanf("%f %f", &num1, &num2) != 2) {
        printf("Invalid input! Please enter numeric values.\n");

        while (getchar() != '\n');

        goto start;
    }

    
    if (num2 == 0) {
        printf("Error: Division by zero is not allowed.\n");
        goto start;
    }


    printf("Result = %.2f\n", num1 / num2);

    return 0;
}
```
## output
<img width="815" height="531" alt="image" src="https://github.com/user-attachments/assets/a79b1448-e675-496f-812d-b9916ae13b3b" />

## 4. Write a C program for a number guessing game where the loop continues for wrong guesses, breaks on a correct guess, and exits the program using return if the user enters -1.

```
#include <stdio.h>

int main() {
    int target = 7;  
    int guess;

    printf("Number Guessing Game!\n");
    printf("Guess the number (Enter -1 to exit)\n");

    while(1) {
        printf("Enter your guess: ");
        scanf("%d", &guess);

        if(guess == -1) {
            printf("You exited the game.\n");
            return 0;
        }

        
        if(guess == target) {
            printf("Correct! You guessed the number.\n");
            break;
        }

       
        printf("Wrong guess! Try again.\n");
    }

    return 0;
}
```
## output
<img width="539" height="592" alt="image" src="https://github.com/user-attachments/assets/f0b055b6-25a7-4d63-ad9b-0401944e521f" />

## 5. Write a C program that iterates through an array and, within a loop, uses continue  to skip negative elements, break when a zero is encountered, and return to exit the program if an element greater than 100 is found, then print the resulting behavior for the array {10, -5, 20, 0, 150, 30}.

```
#include <stdio.h>

int main() {
    int arr[] = {10, -5, 20, 0, 150, 30};
    int n = sizeof(arr) / sizeof(arr[0]);

    for(int i = 0; i < n; i++) {

        if(arr[i] > 100) {
            printf("Element greater than 100 found (%d). Exiting program.\n", arr[i]);
            return 0;
        }

        
        if(arr[i] < 0) {
            continue;
        }

        if(arr[i] == 0) {
            printf("Zero encountered. Stopping loop.\n");
            break;
        }

        printf("%d ", arr[i]);
    }

    return 0;
}
```
## ouput
<img width="853" height="395" alt="image" src="https://github.com/user-attachments/assets/b98b0c7f-1a42-4681-8a7b-3eece8473583" />








