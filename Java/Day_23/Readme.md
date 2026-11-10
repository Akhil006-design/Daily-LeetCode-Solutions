# LeetCode 1299 – Replace Elements with Greatest Element on Right Side

## Problem
Given an integer array `arr`, replace every element with the greatest element among the elements to its right. Replace the last element with `-1`.

## Java Solution

```java
class Solution {
    public int[] replaceElements(int[] arr) {
        int max = -1;

        for (int i = arr.length - 1; i >= 0; i--) {
            int current = arr[i];
            arr[i] = max;

            if (current > max) {
                max = current;
            }
        }

        return arr;
    }
}
```

## Example

**Input:**
```text
[17, 18, 5, 4, 6, 1]
```

**Output:**
```text
[18, 6, 6, 6, 1, -1]
```

## Approach
1. Initialize `max` as `-1`.
2. Traverse the array from right to left.
3. Store the current element in a temporary variable.
4. Replace the current element with `max`.
5. Update `max` if the current element is greater.
6. Return the modified array.

## Complexity Analysis
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Key Learning
Array traversal from right to left and maintaining the greatest element seen so far.
