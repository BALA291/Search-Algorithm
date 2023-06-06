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
```
''' 
Program for linear search method to match the item in a list
Developed by: BALAMURUGAN B
RegisterNumber: 212222230016
'''
def linearSearch(array,n,k):
    # write your code for linear search
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1        
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
array.sort()
result = linearSearch(array,n,k)
if (result==-1):
 print(array)
 print("Element not found")
else:
 print(array)
 print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: BALAMURUGAN B
RegisterNumber: 212222230016
'''
def binarySearchIter(array, k, low, high):
    # Write your code here to find the middle value and check if the desired item is above or below the middle value
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1        
    
array = eval(input())
array.sort()
# sort the array
k = eval(input())
result=binarySearchIter(array, k,0,len(array)-1)
#k-item to be searched
if (result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: BALAMURUGAN B
RegisterNumber: 212222230016
'''
def BinarySearch(arr, k, low, high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return BinarySearch(arr, k, low,mid-1)
        else:
            return BinarySearch(arr, k,mid+1, high)
            
    else:
        return -1
        
    # Write your code here for binary search using recursive method
    
    
array= eval(input())
#sort the array
array.sort()
k = eval(input()) # k is the element to be searched for

# use the binary search function to find the result
result =BinarySearch(array, k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
## Output
i)	#Use a linear search method to match the item in a list.
![p3bio](https://github.com/BALA291/Search-Algorithm/assets/120717501/249b2f33-d09e-4a6a-81a8-455da77fdf5c)
![p3bi](https://github.com/BALA291/Search-Algorithm/assets/120717501/3ba8e2bc-67a4-408e-9c98-3e9c980ceb4c)

ii)	# Find the element in a list using Binary Search(Iterative Method).
![p3biio](https://github.com/BALA291/Search-Algorithm/assets/120717501/9a1863b7-e672-4b91-81d1-4f9afbddb08d)
![p3bii](https://github.com/BALA291/Search-Algorithm/assets/120717501/0f902271-5106-4e34-8fd7-c9be730217d3)

iii)	# Find the element in a list using Binary Search (recursive Method).
![p3biiio](https://github.com/BALA291/Search-Algorithm/assets/120717501/966312af-34fb-4733-9cb0-50d30f9535ae)
![p3biii](https://github.com/BALA291/Search-Algorithm/assets/120717501/ba590372-0a0e-4c83-b77f-b8043dbd8577)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
