# EX 1C Quick Sort
## DATE:
## AIM:
To write a python program to implement quick sort using the first element as pivot value.

## Algorithm
1. Choose a pivot element (typically the first element of the subarray).
2. Partition the array by moving elements smaller than the pivot to the left and larger ones to the right.
3. Recursively apply Quick Sort to the left subarray (quick(a, st, p)).
4. Recursively apply Quick Sort to the right subarray (quick(a, p+1, en)).
5. Repeat partitioning and sorting for smaller subarrays until the entire array is sorted.
6. In the partition step, swap elements so that elements smaller than the pivot are on the left, and larger elements are on the right.
7. Return the sorted array once all partitions are processed.


## Program:
```

Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: SANJAY C
Register Number:  212223240150
```
```PY
def quick_sort(alist, start , end):
    if end - start >1:
        p = partition(alist,start,end)
        quick_sort(alist, start , p)
        quick_sort(alist, p+1 , end)
def partition(alist, start , end):
    pivot = alist[start]
    i = start + 1
    j = end - 1
    print("pivot: ",pivot)
    while True:
        while i <= j and alist[i] <= pivot:
            i = i+1
        while i <= j and alist[j] >= pivot:
            j = j-1
        if i<=j:
            alist[i],alist[j] = alist[j],alist[i]
        else:
            alist[start],alist[j] = alist[j],alist[start]
            return j
n = int(input())
alist = [float(input()) for _ in range(n)]
print("Input List")
print(f" {alist}")
quick_sort(alist, 0 , len(alist))
print("Sorted List")
print(f" {alist}")
```

## Output:

![image](https://github.com/user-attachments/assets/1c245aae-b53f-4826-aa2a-3ad275831ab7)


## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
