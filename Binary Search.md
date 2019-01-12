From https://www.geeksforgeeks.org/binary-search/

### About Binary Search
Given a sorted array arr[] of n elements, write a function to search a given element x in arr[].
A simple approach is to do linear search.The time complexity of above algorithm is **O(n)**. Another approach to perform the same task is using Binary Search.

**Binary Search:** Search a sorted array by repeatedly dividing the search interval in half. The idea of binary search is to use the information that the array is sorted and reduce the time complexity to **O(Log n)**.

1. Begin with an interval covering the whole array. 
2. If the value of the search key is less than the item in the middle of the interval, narrow the interval to the lower half. Otherwise narrow it to the upper half. 
3. Repeatedly check until the value is found or the interval is empty.

### Code to apply Binary Search (Python)

``` python 3
def BinarySearch(List_input, index_now, target):

    if List_input[index_now]==target:
        return index_now

    elif List_input[index_now] > target:
        index_next = index_now+len(List_input[(index_now+1):])//2
        return BinarySearch(List_input, index_next,target)

    else:
        index_next = index_now+len(List_input[(index_now+1):])//2
        return BinarySearch(List_input, index_next ,target)

print(BinarySearch([2, 3, 4, 10, 40 ], 0, 10))
```
Output: 3


 



