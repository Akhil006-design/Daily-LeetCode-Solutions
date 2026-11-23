# LeetCode 2006 – Count Number of Pairs With Absolute Difference K

**Difficulty:** Easy

## Problem
Count the number of pairs whose absolute difference is equal to the given value `k`.

## Approach
1. Initialize count as 0.
2. Use two nested loops.
3. Compare each element with the elements after it.
4. Check whether their absolute difference equals k.
5. Increase count when the condition is satisfied.
6. Return count.

## Java Solution

```java
class Solution {
    public int countKDifference(int[] nums, int k) {
        int count = 0;

        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (Math.abs(nums[i] - nums[j]) == k) {
                    count++;
                }
            }
        }

        return count;
    }
}
```

## Complexity
- Time Complexity: O(n²)
- Space Complexity: O(1)

## Key Learning
- Array traversal
- Nested loops
- Counting pairs
- Math.abs()
- Using count++