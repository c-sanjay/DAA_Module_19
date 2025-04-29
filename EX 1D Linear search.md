# EX 1D Linear search
## DATE:
## AIM:
To write a python program for a search function with parameter list name and the value to be searched on the given list of float values.



## Algorithm
1. Input the list of numbers and the search target n.
2. Iterate through the list, comparing each element with n.
3. If a match is found, return 1 to indicate the number is found.
4. If the end of the list is reached without a match, return -1 indicating the number is not found.
5. Print the result based on whether the number was found or not.

## Program:
```PY
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: SANJAY C
Register Number:  212223240150
*/

def search(List, n):
    for i in List:
        if i == n:
            return 1
            
    return -1

arr = int(input())
List = []
for _ in range(arr):
    List.append(float(input()))
n = float(input())
if search(List, n)==1:
    print(n,"Found")
else:
    print(n,"Not Found")

```

## Output:

![image](https://github.com/user-attachments/assets/57ed2350-23db-410b-9f04-a215704e8883)


## Result:
The program was executed successfully, and it correctly checks if the input element is present in the list, printing "Found" if the element exists or "Not Found" if it does not.
