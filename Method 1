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
