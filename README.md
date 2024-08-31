Smallest Sub-array with sum greater than a given value in Python
Here, on this page, we will discuss the program to find Smallest Sub-array with sum greater than a given value in Python programming language. We are given an unsorted array containing non-negative integers we need to find a continuous sub-array of minimum length whose sum is greater than the given sum

Example :

Input : arr : [ 1, 4, 0, 0, 2, 6, 3 ] & sum = 6
Output : Sub-array with sum greater than 6 will have a size of 2 Elements
Explanation : For the given array. The sub-array from index 4 to 5 will give a sum of 8 (2+6), greater than the value  6, and the smallest subarray with a sum greater than the given sum.
Smallest Sub-array with sum greater than a given value in Python

Algorithm
Initialize a variable ans with any value greater than length of array
Iterate using a for loop from 0 to l with i
Initialize a variable sum = 0
Run a nested for loop from i to l with j
For each iteration add arr[j] to sum, check if sum is greater than x, check if ans is greater than j-i put j-i to ans
After coming out of the loop check if ans is greater than l print “Not possible” else return ans +1
Python Code
Run
def sub(arr, x, l):
    ans = l+1
    for i in range(l):
        sum = 0
        for j in range(i, l):
            sum += arr[j]
            if sum > x:
                if (j - i) < ans:
                    ans = j - i
    if ans > l:
        return "NOT POSSIBLE"
    else:
        return ans + 1


arr = [1, 2, 3, 4, 5]
x = 5
l = len(arr)
print("Sub-array with sum greater than", x, "will have a size of", sub(arr, x, l), "Elements for given array")
Output
Sub-array with sum greater than 5 will have a size of 2 Elements for given array
