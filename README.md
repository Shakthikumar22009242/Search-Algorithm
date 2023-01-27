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
i)	#Use a linear search method to match the item in a list.
```python
''' 
Program for linear search method to match the item in a list
Developed by: Shakthi kumar S
RegisterNumber: 22009242
'''
def linearSearch(array,k):
    for i in range(len(array)):
        if array[i]==k:
            return True
    return False
array = eval(input())
k = eval(input())
array.sort()
print(array)
if linearSearch(array,k):
    print("Element found at index: ",array.index(k))
else:
    print("Element not found")
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Shakthi kumar S
RegisterNumber: 22009242
'''
def binarySearchIter(array, k, low, high):
    while low<=high:
        middle=low+(high-low)//2
        if array[middle]==k:        
            return True
        elif array[middle]<k:
            low=middle+1
        else:
            high=middle-1
    return False
array=eval(input())
array.sort()
k = eval(input())
print(array)
low=0
high=len(array)-1
if binarySearchIter(array,k,low,high):
    print("Element found at index: ",array.index(k))
else:
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Shakthi kumar S
RegisterNumber: 22009242
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return -1
arr=eval(input())
arr.sort()
k=eval(input())
result=BinarySearch(arr,k,0,len(arr)-1)
if result==-1:
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ",result)
```
## Sample Input and Output
![](linear_search.png)
![](binary.png)
![](Binary_recursion.png)
## Result
Thus the linear search and binary search algorithm is implemented using python programming.