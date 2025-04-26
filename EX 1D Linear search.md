# EX 1D Linear search
## AIM:
Write a Python program to search for an element in a list using Linear Search.
## Algorithm
1.Input a (number of elements).

2.Read a elements into the list List.

3.Input the element n to search for.

4.Define a function search(list, n):

5.For each element i in list:

6.If i == n, print "n Found" and break.

7.Else (if no break happens), print "n Not Found".

8.Call search(List, n). 

## Program:
```
/*
Program to implement a search function with parameter list name and the value to be searched using string values.
Developed by: lingaraja l
Register Number:  212222040086
*/
```
```
def search(list, n):
    for i in list:
        if i == n:
            print(f"{n} Found")
            break
    else:
        print(f"{n} Not Found")

a = int(input())
List = []
for i in range(a):
    List.append(float(input()))

n = float(input())
search(List, n)

```

## Output:

![Screenshot 2025-04-26 141227](https://github.com/user-attachments/assets/552c1f0a-85d5-4c0d-895e-d148c004447c)


## Result:
The program successfully searches for the given element using Linear Search.
