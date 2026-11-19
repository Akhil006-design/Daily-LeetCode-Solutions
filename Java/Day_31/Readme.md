# LeetCode 1550 – Three Consecutive Odds

**Difficulty:** Easy

## Problem
Given an integer array, return `true` if the array contains three consecutive odd numbers. Otherwise, return `false`.

## Approach
1. Traverse the array using a for loop.
2. Check three consecutive elements.
3. If all three are odd, return `true`.
4. If no such group exists, return `false`.

## Java Solution

```java
class Solution {
    public boolean threeConsecutiveOdds(int[] arr) {
        for (int i = 0; i < arr.length - 2; i++) {
            if (arr[i] % 2 != 0 &&
                arr[i + 1] % 2 != 0 &&
                arr[i + 2] % 2 != 0) {
                return true;
            }
        }

        return false;
    }
}
```

## Complexity
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Key Learning
- Checking odd and even numbers using `%`.
- Traversing arrays.
- Checking consecutive elements.