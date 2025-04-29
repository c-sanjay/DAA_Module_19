# EX 1B Merge Sort
## DATE:
## AIM:
To write a python program to sort the first half of the list using merge sort.

## Algorithm

1. Divide the array into two halves at the middle index m = (l + r) // 2
2. Recursively sort the left half of the array (mergeSort(arr, l, m)).
3. Recursively sort the right half of the array (mergeSort(arr, m+1, r)).
4. Merge the two sorted subarrays using the merge() function.
5. Compare elements from the left and right subarrays and insert the smaller one into the merged array.
6. Copy any remaining elements from the left or right subarrays into the merged array.
7. Return the sorted array once all subarrays are merged.

## Program:
```
/*
Program to implement Merge Sort
Developed by: SANJAY C
Register Number: 212223240150
*/
def merge(arr, l, m, r):
    n1 = m - l + 1
    n2 = r - m
    L = [0] * (n1)
    R = [0] * (n2)
    for i in range(0, n1):
        L[i] = arr[l + i]
 
    for j in range(0, n2):
        R[j] = arr[m + 1 + j]
 

    i = 0     
    j = 0     
    k = l     
 
    while i < n1 and j < n2:
        if L[i] <= R[j]:
            arr[k] = L[i]
            i += 1
        else:
            arr[k] = R[j]
            j += 1
        k += 1
 

    while i < n1:
        arr[k] = L[i]
        i += 1
        k += 1
 
    while j < n2:
        arr[k] = R[j]
        j += 1
        k += 1

def mergeSort(arr, l, r):
    if l < r:
        m = l+(r-l)//2
        mergeSort(arr, m+1, r)
        merge(arr, l, m, r)
 

arr =[]              
n =int(input())
for i in range(n):
    arr.append(int(input()))
print("Given array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
 
mergeSort(arr, 0, n-1)
print("\n\nSorted array is")
for i in range(n):
    print("%d" % arr[i],end=" ")
 
```

## Output:

![image](https://github.com/user-attachments/assets/f8c6980f-a128-4b09-a373-34aee255fa75)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
