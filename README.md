Counting Inversion in Python
On this page we will learn to create program for counting inversion in Python Programing language for a given array. 

Example : –

Input: A = [6, 3, 5, 2, 7]
Output: 5
Explanation: The five pairs of inversions are – (6, 3) , (6, 5), (6, 2), (3, 2), (5, 2)
Count Inversion in Python
Did you know?
  Two elements a[i] and a[j] form an inversion only if a[i] > a[j] and i < j.

Inversion count of a number means how close the array is to be sorted
If the array is already sorted the inversion count of the array will be zero
If the array is sorted in reverse order inversion count will be maximum
Algorithm
Initialize a variable ans assign 0
Iterate using for loop from 0 to length of array using variable i
Run a nested for loop from i+1 to length of array using variable j
If element at jth position is smaller then element at ith position in array then increment the value of ans by 1
Python Code
Run
def inversion(arr):
    ans = 0
    for i in range(len(arr)):
        for j in range(i + 1, len(arr)):
            if arr[j] < arr[i]:
                ans += 1
    return ans


array = [6, 3, 5, 2, 7]
print("There are", inversion(array), "possible inversion")
Python Code
There are 5 possible inversion
