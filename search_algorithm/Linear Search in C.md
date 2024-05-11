Here's an example of linear search implemented in C:

```
#include <stdio.h>

int linear_search(int arr[], int n, int target) {
    // Iterate through the array
    for (int i = 0; i < n; i++) {
        // Check if the current element matches the target
        if (arr[i] == target) {
            return i; // Return the index if target is found
        }
    }
    return -1; // Return -1 if target is not found
}

int main() {
    int arr[] = {5, 3, 8, 2, 9, 1};
    int n = sizeof(arr) / sizeof(arr[0]); // Calculate the size of the array
    int target = 8;
    int result = linear_search(arr, n, target);
    if (result != -1) {
        printf("Target %d found at index %d.\n", target, result);
    } else {
        printf("Target %d not found in the array.\n", target);
    }
    return 0;
}
``` 

In this C implementation, the `linear_search` function takes an integer array `arr`, the size of the array `n`, and the target value `target`. It iterates through each element of the array using a `for` loop and compares each element with the target value. If a match is found, it returns the index of the target element. If the target element is not found after iterating through the entire array, it returns -1.

The `main` function demonstrates how to use the `linear_search` function by passing an array, its size, and the target value. It then prints the result based on whether the target was found or not.