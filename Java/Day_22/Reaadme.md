# LeetCode 1464 – Maximum Product of Two Elements in an Array

## Problem
Given an integer array `nums`, find the maximum value of `(nums[i] - 1) * (nums[j] - 1)` where `i` and `j` are different indices.

## Java Solution

```java
class Solution {
    public int maxProduct(int[] nums) {
        int max1 = 0;
        int max2 = 0;

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] > max1) {
                max2 = max1;
                max1 = nums[i];
            } else if (nums[i] > max2) {
                max2 = nums[i];
            }
        }

        return (max1 - 1) * (max2 - 1);
    }
}
```

## Example

**Input:**
```text
nums = [3,4,5,2]
```

**Output:**
```text
12
```

**Explanation:** The two largest numbers are 5 and 4.

`(5 - 1) * (4 - 1) = 12`

## Approach
1. Initialize two variables to store the largest and second-largest numbers.
2. Traverse the array.
3. Update the two largest values.
4. Multiply `(max1 - 1)` and `(max2 - 1)`.

## Complexity
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Key Learning
Finding the two largest elements in an array using a single loop.
