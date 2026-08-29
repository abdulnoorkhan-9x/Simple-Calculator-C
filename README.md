# Simple-Calculator-C
A console based calculator in C that performs addition, subtraction, multiplication and division using switch-case statement | BCA Project | C Programming

# 🔢 Simple Calculator C

## 📌 About This Project
A console-based calculator in C that
performs basic mathematical operations.

## 🎯 Features
- Addition ➕
- Subtraction ➖
- Multiplication ✖️
- Division ➗
- Division by zero error handling ⚠️

## 💡 Why I Built This
This project helped me understand:
- Switch statements for menu selection
- Float data type for decimal numbers
- Arithmetic operators in C
- Error handling (division by zero)

## 📊 Sample Output
===== SIMPLE CALCULATOR =====
1. Addition
2. Subtraction
3. Multiplication
4. Division
Enter your choice: 1
Enter first number: 10
Enter second number: 5
10.00 + 5.00 = 15.00

## 📚 Concepts Used
- switch-case statement
- float data type
- Arithmetic operators (+, -, *, /)
- if-else for error handling
- scanf() for multiple inputs
- printf() with formatting (%.2f)

## 🔗 Real World Connection
Every calculator app — Phone calculator,
scientific calculator — uses same logic!
This is the foundation of all calculators!

## ⏱️ Time Taken To Build
- Concept understanding: 20 minutes
- Coding: 30 minutes
- Testing all operations: 15 minutes
- Total: 1 hour 5 minutes

## 💻 Technologies Used
- C Programming Language
- GCC Compiler

## 🚀 Future Improvements
- Add modulus operation
- Add power calculation
- Add square root

## 🔧 How To Run
1. Install GCC compiler
2. Save as calculator.c
3. Compile: gcc calculator.c -o calc
4. Run: ./calc

## 👨‍💻 Author
Abdul Noor Khan
BCA Student | City Group of Colleges, Lucknow




#include<stdio.h>
void main()
{
    float num1, num2, result;
    int choice;
    
    printf("===== SIMPLE CALCULATOR =====\n");
    printf("1. Addition\n");
    printf("2. Subtraction\n");
    printf("3. Multiplication\n");
    printf("4. Division\n");
    printf("Enter your choice: ");
    scanf("%d", &choice);
    
    printf("Enter first number: ");
    scanf("%f", &num1);
    printf("Enter second number: ");
    scanf("%f", &num2);
    
    switch(choice)
    {
        case 1:
            result = num1 + num2;
            printf("%.2f + %.2f = %.2f", 
                   num1, num2, result);
            break;
            
        case 2:
            result = num1 - num2;
            printf("%.2f - %.2f = %.2f", 
                   num1, num2, result);
            break;
            
        case 3:
            result = num1 * num2;
            printf("%.2f x %.2f = %.2f", 
                   num1, num2, result);
            break;
            
        case 4:
            if(num2 != 0)
            {
                result = num1 / num2;
                printf("%.2f / %.2f = %.2f",
                       num1, num2, result);
            }
            else
            {
                printf("Error! Division by zero!");
            }
            break;
            
        default:
            printf("Invalid choice!");
    }
}
