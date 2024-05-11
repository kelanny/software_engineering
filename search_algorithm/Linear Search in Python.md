```
def linear_search(arr, target):
    """
    Perform linear search to find the target element in the given array.

    Parameters:
    - arr: A list or array to search through.
    - target: The element to search for.

    Returns:
    - The index of the target element if found, or -1 if not found.
    """
    for i in range(len(arr)):
        if arr[i] == target:
            return i  # Return the index if target is found
    return -1  # Return -1 if target is not found
```

# Example usage:
arr = [5, 3, 8, 2, 9, 1]
target = 8
result = linear_search(arr, target)
if result != -1:
    print(f"Target {target} found at index {result}.")
else:
    print(f"Target {target} not found in the array.")
