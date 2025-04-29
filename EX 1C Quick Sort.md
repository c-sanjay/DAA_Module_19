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
def quick(a,st,en):
    if en-st>1:
        p=partition(a,st,en)
        quick(a,st,p)
        quick(a,p+1,en)
def partition(a,st,en):
    pivot=a[st]
    i=st+1
    j=en-1
    print("Pivot: ",pivot)
    while True:
        while(i<=j and a[i]<=pivot):
            i=i+1
        while(i<=j and a[j]>=pivot):
            j=j-1
        if i<=j:
            a[i],a[j]=a[j],a[i]
        else:
            a[st],a[j]=a[j],a[st]
            return j

a=[]
n=int(input())
for i in range(n):
    a.append(int(input()))
quick(a,0,len(a))
print("Sorted array:",a)

```

## Output:

![image](https://github.com/user-attachments/assets/04041b6c-24bd-42d2-9c85-d5526da27023)


## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
