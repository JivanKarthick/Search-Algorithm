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
Program for linear search method to match the item in a list
Developed by:Jivan Karthec.B.S
RegisterNumber: 22004763

def linearsearch(array,n,k):
    for i in range(0,n):
        if (array[i] == k):
            return i
    return -1
array = eval(input())
k = eval(input())
n = len(array)
array.sort()
result = linearsearch(array,n,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
    
```

ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarySearchIter(array,k,low,high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return-1
array=eval(input())
array.sort()
k = eval(input())
result = binarySearchIter(array,k,0,len(array)-1)
if result==-1:
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
Developed by:Jivan Karthec.B.S
RegisterNumber: 22004763
'''
def BinarySearch(arr,k,low,high):
    if low <= high:
        mid = low + (high - low)//2
        if array[mid] == k:
            return mid
        elif array[mid] > k:
            return  BinarySearch(arr,k,low,mid-1) 
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return-1
array=eval(input())
array.sort()
k = eval(input())
result = BinarySearch(array,k,0,len(array)-1)
if result==-1:
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
        



```
## Sample Input and Output
![1](https://user-images.githubusercontent.com/121165867/214817576-5f92f22f-f777-4190-9422-f191768d6119.png)
![2](https://user-images.githubusercontent.com/121165867/214817597-5ee0f385-0124-4e9b-b135-a4ae6559f107.png)
![2](https://user-images.githubusercontent.com/121165867/214817613-0846d5d1-f562-435e-9e15-2ae6d4d7e3b2.png)






## Result
Thus the linear search and binary search algorithm is implemented using python programming.
