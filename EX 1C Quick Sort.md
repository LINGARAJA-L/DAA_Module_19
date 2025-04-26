# EX 1C Quick Sort
## AIM:
Write a Python program to sort an array using the Quick Sort algorithm.

## Algorithm
1.Read input n (number of elements).

2.Read n elements into list a.

3.Call quick(a, 0, n) to sort the list:

4.If the size of the subarray is more than 1:

5.Partition the array using partition(a, st, en):

6.Set the pivot element as the first element.

7.Move elements smaller than pivot to its left, greater to its right.

8.Place pivot at correct position.

9.Recursively call quick on left and right parts.

10.Print the sorted array.

## Program:
```
/*
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: lingaraja l
Register Number:  212222040086
*/
```
```
def quick(a, st, en):
    if en - st > 1:
        p = partition(a, st, en)
        quick(a, st, p)
        quick(a, p + 1, en)

def partition(a, st, en):
    pivot = a[st]
    i = st + 1
    j = en - 1
    while True:
        while i <= j and a[i] <= pivot:
            i += 1
        while i <= j and a[j] >= pivot:
            j -= 1
        if i <= j:
            a[i], a[j] = a[j], a[i]
        else:
            a[st], a[j] = a[j], a[st]
            return j

a = []
n = int(input())
for i in range(n):
    a.append(int(input()))

quick(a, 0, len(a))
print(a)

```

## Output:
![Screenshot 2025-04-26 140843](https://github.com/user-attachments/assets/6b56a2cd-14a3-4668-a308-c4884ffdcdd7)

## Result:
The program successfully sorts the given array using the Quick Sort algorithm.
