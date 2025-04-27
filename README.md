# Adv-C-Mod-8

EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER 

Aim: To write a C program print the lowercase English word corresponding to the number 

Algorithm:
Start

Initialize an integer variable n.

Input Validation

Switch Statement cases.

Case 5: Print "seventy one"

Case 6: Print "seventy two"

Case 13: Print "seventy three"

...

Case 13: Print "seventy nine"

Default: Print "Greater than 79"

Exit the program.

Program:
```
#include <stdio.h>
int main(){
    int n;
    scanf("%d",&n);
    if(n==71){
        printf("seventy one");
    }
    else if(n==72){
        printf("seventy two");
    }
    else if(n==73){
        printf("seventy three");
    }
    else if(n==74){
        printf("seventy four");
    }
    else if(n==75){
        printf("seventy five");
    }
    else if(n==76){
        printf("seventy six");
    }
    else if(n==77){
        printf("seventy seven");
    }
    else if(n==78){
        printf("seventy eight");
    }
    else if(n==79){
        printf("seventy nine");
    }
    else if(n>79){
        printf("Greater than 49");
    }
}
```


Output:

![image](https://github.com/user-attachments/assets/485174f7-72b8-4695-814e-b387b4bb2066)

Result: 

Thus, the program is verified successfully


EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS IN A SINGLE LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 . 

Aim: To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3. 

Algorithm:

Start

Declare char array a[50] outer loop for each digit from 0 to 3

Initialize counter c to 0

For each character in the string print count c for current digit, followed by a space

Increment h to move to the next digit

End

Program:
```
#include <stdio.h>
#include <string.h>

int main() {
    int sum, i, j;
    char str[20];
    
    scanf("%s", str);
    int length = strlen(str);

    for (i = 0; i < 4; i++) {
        sum = 0; 
        for (j = 0; j < length; j++) {
            if (str[j] == '0' + i) {  
                sum++;
            }
        }
        printf("%d ", sum);
    }

    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/6a2248e9-8ab4-46ef-9f53-b3a2c3b448a5)

Result: 

Thus, the program is verified successfully


EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER. 

Aim: To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:

Start

Declare variables s (pointer to an array of strings) and n (number of strings)

Memory Allocation Dynamically allocate memory for s to store an array of strings

Input Read the number of strings n from the user Dynamically allocate memory for each string in s

Permutation Generation Loop

Memory Deallocation Free the memory allocated for each string in s Free the memory allocated for s

End

Program:

```
#include <stdio.h>
#include <string.h>

int main() {
    int n, i, j;
    scanf("%d", &n);
    char a[n][20], temp[20];
    for (i = 0; i < n; i++) {
        scanf("%s", a[i]);
    }
    for (i = 0; i < n - 1; i++) {
        for (j = i + 1; j < n; j++) {
           if (strcmp(a[i], a[j]) > 0) {
                strcpy(temp, a[i]);
                strcpy(a[i], a[j]);
                strcpy(a[j], temp);
            }
        }
    }

    for (i = 0; i < n; i++) {
        printf("%s ", a[i]);
    }
    printf("\n");
    while (1) {
        int i = n - 2;
        while (i >= 0 && strcmp(a[i], a[i + 1]) >= 0) {
            i--;
        }
        if (i < 0) {
            break;
        }
        int j = n - 1;
        while (strcmp(a[i], a[j]) >= 0) {
            j--;
        }
        strcpy(temp, a[i]);
        strcpy(a[i], a[j]);
        strcpy(a[j], temp);
        int start = i + 1;
        int end = n - 1;
        while (start < end) {
            strcpy(temp, a[start]);
            strcpy(a[start], a[end]);
            strcpy(a[end], temp);
            start++;
            end--;
        }
        for (i = 0; i < n; i++) {
            printf("%s ", a[i]);
        }
        printf("\n");
    }

    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/cb0e9124-b2d9-44da-bf57-faaee0de13f6)


Result: 

Thus, the program is verified successfully

EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS SHOWN BELOW. 

Aim: To write a C program to print a pattern of numbers from 1 to n as shown below. 

Algorithm:

Start

Declare integer variables n, i, j, min

Read the value of n from the user

Calculate the length of the side of the square matrix: len = n * 2 - 1

Matrix Generation Loop

Calculate min as the minimum distance to the borders

End

Program:
```
#include <stdio.h>

int main() {
    int n, i, j;
    scanf("%d", &n);
    for (i = 0; i < (2 * n) - 1; i++) {
        for (j = 0; j < (2 * n) - 1; j++) {
            int min = i < j ? i : j;
            min = min < (2 * n - 2 - i) ? min : (2 * n - 2 - i);
            min = min < (2 * n - 2 - j) ? min : (2 * n - 2 - j);
            printf("%d ", n - min);
        }
        printf("\n");
    }

    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/542d7b23-283c-45b3-be90-06ba74fbca14)


Result: 

Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

Start.

Define a function square() with no parameters. This function will return an integer value.

Inside the function: o Declare an integer variable to store the number. o Ask the user to input a number. o Calculate the square of the number (multiply 
the number by itself). 

o Return the squared value.

In the main function: o Call the square() function and display the result.

End.

Program:

```
#include <stdio.h>

int square();

int main() {
    int result;
    
    result = square();
    
    printf("The square of the number is: %d\n", result);
    
    return 0;
}


int square() {
    int num;
    
    
    scanf("%d", &num);
    
    return num * num;
}
```

Output:

![image](https://github.com/user-attachments/assets/d4163442-4472-4ef8-8741-024897c2afe5)


Result: 

Thus, the program is verified successfully
