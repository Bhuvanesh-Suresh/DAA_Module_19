# EX 1C Quick Sort
## DATE: 01-03-2025
## AIM:To Write a python program to implement quick sort on the given values and print the sorted list and pivot value of each iteration

## Algorithm
1. Select a pivot element from the array (commonly the first or last element).
2. Partition the array into two subarrays: elements less than pivot and elements greater than or equal to pivot.
3. Place the pivot between the two subarrays at its correct position.
3. Recursively apply Quick Sort to the left subarray.
4. Recursively apply Quick Sort to the right subarray. 

## Program:
```
Program to implement implement quick sort using the last element as pivot on the list of float values.
Developed by: Bhuvanesh S R
Register Number: 212223240017
```
```py
def partition(array, low, high):
    pivot = array[low]
    start = low + 1
    end = high
    print("pivot: ",pivot)
    while True:
        while start <= end and array[end] >= pivot:
            end = end - 1
        while start <= end and array[start] <= pivot:
            start = start + 1
        if start <= end:
            array[start], array[end] = array[end], array[start]
        else:
            break
    array[low], array[end] = array[end], array[low]
    return end
def quick_sort(array, start, end):
    if start < end:
        idx = partition(array, start, end)
        quick_sort(array, start, idx-1)
        quick_sort(array, idx+1, end)
arr1=[]
n=int(input())
for i in range(n):
    arr1.append(int(input()))
print("Input List\n",arr1)
quick_sort(arr1, 0, len(arr1)-1)
print("Sorted List\n",arr1)
 ```

## Output:
![image](https://github.com/user-attachments/assets/75323b1a-fbd5-4215-9496-2a0225622ada)





## Result:
The program successfully sorts the input array using the QuickSort algorithm, arranging the elements in ascending order.
