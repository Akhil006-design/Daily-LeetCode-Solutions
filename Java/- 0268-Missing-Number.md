# LeetCode 268 — Missing Number

## Problem
Given an array containing `n` distinct numbers from the range `[0, n]`, return the only number in the range that is missing from the array.

**Problem Link:** https://leetcode.com/problems/missing-number/

## Example

**Input:**
```text
nums = [3, 0, 1]
```

**Output:**
```text
2
```

**Explanation:** The numbers from `0` to `3` are `0, 1, 2, 3`. The number `2` is missing.

## Approach: Sum Formula

The sum of numbers from `0` to `n` is:

`n * (n + 1) / 2`

Subtract the actual array sum from the expected sum to find the missing number.

## Java Solution

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n = nums.length;
        int expectedSum = n * (n + 1) / 2;
        int actualSum = 0;

        for (int num : nums) {
            actualSum += num;
        }

        return expectedSum - actualSum;
    }
}
```

## Code Explanation

1. `nums.length` gives the number of elements in the array.
2. `expectedSum` calculates the sum of all numbers from `0` to `n`.
3. `actualSum` stores the sum of the numbers present in the array.
4. The enhanced `for` loop adds every array element to `actualSum`.
5. `expectedSum - actualSum` returns the missing number.

## Complexity Analysis

- **Time Complexity:** `O(n)` — the array is traversed once.
- **Space Complexity:** `O(1)` — only a constant amount of extra space is used.

## What I Learned

- How to traverse an array using an enhanced `for` loop.
- How to use the arithmetic sum formula.
- How to solve an array problem efficiently using mathematics.
