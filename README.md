# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
# Step 1:
Start from the leftmost element of array[] and compare k with each element of array[] one by one.
# Step 2:
If k matches with an element in array[] , return the index.
# Step 3:
If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
# Step 1:
Set two pointers low and high at the lowest and the highest positions respectively.
# Step 2:
Find the middle element mid of the array ie. arr[(low + high)/2]
# Step 3:
If x == mid, then return mid.Else, compare the element to be searched with m.
# Step 4:
If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
# Step 5:
Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
# Step 6:
Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
'''to search the item in a list one by one from start to end to find the match. 
(or) Use a linear search method to match the item in a list.'''
#Developed by: LOGA MITHRA.R
#Register number: 212223100027
def search(lst,n,x):
    for i in range(0,n):
        if(lst[i]==x):
            return i
    return -1
lst=eval(input())
x=eval(input())
n=len(lst)
lst.sort()
ans=search(lst,n,x)
if ans==-1:
    print(lst)
    print("Element not found")
else:
    print(lst)
    print("Element found at index: ",ans)
```

ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#to find the element in a list using Binary Search(Iterative Method).
#Developed by: LOGA MITHRA.R
#Register number: 212223100027
def binary(lst,n,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if lst[mid]==n:
            return mid
        elif lst[mid]<n:
            low=mid+1
        else:
            high=mid-1
    return -1
lst=eval(input())
lst.sort()
n=eval(input())
ans=binary(lst,n,0,len(lst)-1)
if ans==-1:
    print(lst)
    print("Element not found")
else :
    print(lst)
    print("Element found at index: ",ans)
```

iii)	# Find the element in a list using Binary Search (recursive Method).
```
#to find the element in a list using Binary Search (recursive Method).
#Developed by: LOGA MITHRA.R
#Register number: 212223100027
def binary(lst,n,low,high):
    if (low<=high):
        mid=low+(high-low)//2
        if lst[mid]==n:
            return mid
        elif lst[mid]<n:
            low=mid+1
            return binary(lst,n,low,high)
        else:
            high=mid-1
            return binary(lst,n,low,high)
    return -1
lst=eval(input())
lst.sort()
n=eval(input())
ans=binary(lst,n,0,len(lst)-1)
if ans==-1:
    print(lst)
    print("Element not found")
else :
    print(lst)
    print("Element found at index: ",ans)
```
## Sample Input and Output
![output](/img%201.png)

![output](/img%202.png)

![output](/img%203.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
