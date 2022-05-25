#Linear search in python

def linearSearch(array, n, x):

    for i in range(0, n):
        if (array[i] == x):
            return i
    return -1


# Binary Search in python

def binarySearch(array, x, low, high):

    while low <= high:

        mid = low + (high - low)//2

        if array[mid] == x:
            return mid

        elif array[mid] < x:
            low = mid + 1

        else:
            high = mid - 1

    return -1

# bubble sort in python

def bubblesort(array):
 
  for n in range(len(array)-1, 0, -1):
    for i in range(n):
      if array[i] > array[i + 1]:
        array[i], array[i + 1] = array[i + 1], array[i]


# Insertion sort in Python


def insertionSort(array):

    for step in range(1, len(array)):
        key = array[step]
        j = step - 1
        
              
        while j >= 0 and key < array[j]:
            array[j + 1] = array[j]
            j = j - 1
        
        
        array[j + 1] = key


#for fibonacci series
def recur_fibo(n):
   if n <= 1:
       return n
   else:
       return(recur_fibo(n-1) + recur_fibo(n-2))



array = []
  

n = int(input("Enter number of elements : "))
  

for i in range(0, n):
    ele = int(input())
    array.append(ele) 
      
print(array)

x = int(input("Enter the number you want to search"))
n = len(array)
#for linear search
result = linearSearch(array, n, x)
if(result == -1):
    print("Element not found")
else:
    print("Element found at index: ", result)
#for binary search   
result = binarySearch(array, x, 0, len(array)-1)
if result != -1:
    print("Element is present at index " + str(result))
else:
    print("Not found")

#for bubblesort
print("Unsorted list is,") 
print(array)
bubblesort(array)
print("Sorted Array is, ")
print(array)

#for insertion sort
insertionSort(array)
print('Sorted Array in Ascending Order:')
print(array)

#for fibonacci series
nterms=int(input("enter the number for fibonacci sequence"))
if nterms <= 0:
   print("Plese enter a positive integer")
else:
   print("Fibonacci sequence:")
   for i in range(nterms):
       print(recur_fibo(i))
