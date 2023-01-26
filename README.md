# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
### i)	Use a linear search method to match the item in a list.
```py
#Program for linear search method to match the item in a list
#Developed by: Sanjay Ragavendar M K
#RegisterNumber: 22009286

def linearSearch(array,n,k):
    for i in range (n-1):
        if k==array[i]:
            return i
    return -1
array = eval(input())
array.sort()
k = eval(input()) # k-item to be seared for
n = len(array)
result = linearSearch(array,n,k)
print(array)
if result == -1:
    print('Element not found')
else:
    print('Element found at index: ',result)
```
### ii)	 Find the element in a list using Binary Search(Iterative Method).
```py
#Program to find the element in a list using Binary Search(Iterative Method)..
#Developed by: Sanjay Ragavendar M K
#RegisterNumber: 22009286

def binarySearchIter(array, k, low, high):
    while low<=high:
        mid = low + (high-low)//2
        if array[mid] == k:
            return mid
        elif array[mid]<k:
            low = mid+1
        elif array[mid]>k:
            high = mid-1
    return -1
array = eval(input())
array.sort()
k = eval(input()) 
result=binarySearchIter(array,k,0,len(array)-1)
print(array)
if result==-1:
    print('Element not found')
else:
    print('Element found at index: ',result)
```
### iii) Find the element in a list using Binary Search (recursive Method).
```py
#Program to find the element in a list using Binary Search (recursive Method).
#Developed by: Sanjay Ragavendar M K
#RegisterNumber: 22009286

def BinarySearch(arr, k, low, high):
    if high>=low:
        mid = low +(high-low)//2
        if arr[mid] == k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return -1
arr = eval(input())
arr.sort()
k = eval(input()) # k is the element to be searched for
result=BinarySearch(arr,k,0,len(arr)-1)
print(arr)
if result == -1:
    print('Element not found')
else:
    print('Element found at index: ',result)
```
## Sample Input and Output
### (i)
![image](https://user-images.githubusercontent.com/91368803/214863448-e8a1f3d8-72dc-407c-9248-cea302c4ba4c.png)
### (ii)
![image](https://user-images.githubusercontent.com/91368803/214863574-4f105341-b614-4c06-9133-f7011de7a9d5.png)
### (iii)
![image](https://user-images.githubusercontent.com/91368803/214863696-c6055949-13ba-488a-ad83-f7b5e0331909.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
