# EX 1A Reverse a String
## DATE:
## AIM:
To write a program to create a recursive function to reverse a string.

## Algorithm
1. Define a Function: Create a function named rev that takes one input, which is expected to be a string.
2. Reverse the String: Inside the rev function, use string slicing [::-1] to create a reversed copy of the input string.
3. Return the Reversed String: The rev function returns the newly created reversed string.
4.  Get User Input: The program prompts the user to enter some text using the input() function and stores this input string in a variable named string.
5.   Call the Function and Print
## Program:
```
/*
Program to implement Reverse a String
Developed by: SANJAY C
Register Number: 212223240150 
*/
```
```py
def rev(str):
    return str[::-1]
    
string = input()
result = rev(string)
print(resuLt)
```

## Output:
![Screenshot 2025-04-29 144030](https://github.com/user-attachments/assets/ceebdf6d-bbb5-4f97-b38a-de0ecd455a64)


## Result:
The program successfully reverses the input string using recursion. When the user provides an input string, the output displays the reversed version of the string
