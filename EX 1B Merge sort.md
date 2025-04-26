# EX 1B Merge Sort
## AIM:
Write a Python program to sort an array using the Merge Sort algorithm.

## Algorithm
1.Take input n (number of elements).

2.Read n elements into the array arr.

3.Call mergeSort(arr, 0, n-1) to sort the array:

4.If l < r, find the middle index m.

5.Recursively call mergeSort on the left and right subarrays.

6.Merge the two sorted halves using merge(arr, l, m, r).

7.Display the sorted array.

## Program:
```
/*
Program to implement Merge Sort
Developed by: LINGARAJA L
Register Number:  212222040086
*/
```
```
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

The program successfully sorts the given array using the Merge Sort algorithm.

## Result:
The program successfully sorts the first half of the given array using merge sort. where only the first half is sorted, and the second half remains unchanged.
