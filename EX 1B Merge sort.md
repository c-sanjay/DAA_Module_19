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
Program to implement Merge Sort
Developed by: SANJAY C
Register Number: 212223240150
```
```PY
def merge_sort(inp_arr):
    size=len(inp_arr)
    if size>1:
        middle=size//2
        left_arr=inp_arr[:middle]
        right_arr=inp_arr[middle:]
        merge_sort(left_arr)
        merge_sort(right_arr)
        p=0
        q=0
        r=0
        left_size=len(left_arr)
        right_size=len(right_arr)
        while p<left_size and q<right_size:
            if left_arr[p]<right_arr[q]:
                inp_arr[r]=left_arr[p]
                p+=1
            else:
                inp_arr[r]=right_arr[q]
                q+=1
            r+=1
        while p<left_size:
            inp_arr[r]=left_arr[p]
            p+=1
            r+=1
        while q<right_size:
            inp_arr[r]=right_arr[q]
            q+=1
            r+=1




n=int(input())
inp_arr=[int(input()) for _ in range(n)]
print("Given array is")
print(*inp_arr)
print(" ")
size=len(inp_arr)
size1=size//2
second_half=inp_arr[:size1]
first_half=inp_arr[size:1]
merge_sort(first_half)
inp_arr[:size1]=first_half
inp_arr[size1:]=second_half
print("Sorted array is")
print(*inp_arr)
```

## Output:

![image](https://github.com/user-attachments/assets/f8c6980f-a128-4b09-a373-34aee255fa75)


## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
