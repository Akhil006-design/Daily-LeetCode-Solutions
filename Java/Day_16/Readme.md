# LeetCode 1822 – Sign of the Product of an Array

**Difficulty:** Easy  
**Language:** Java

## Problem
Given an integer array `nums`, find the sign of the product of all its elements.

Return:
- `1` if the product is positive.
- `-1` if the product is negative.
- `0` if the product is zero.

## Java Solution

```java
class Solution {
    public int arraySign(int[] nums) {
        int sign = 1;

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] == 0) {
                return 0;
            }
            else if (nums[i] < 0) {
                sign = sign * -1;
            }
        }

        return sign;
    }
}
```

## Logic – Step by Step

1. Start with `sign = 1`.
2. Traverse the array using a `for` loop.
3. If an element is `0`, return `0`.
4. If an element is negative, multiply `sign` by `-1`.
5. After checking all elements, return `sign`.

## Example

**Input:**
```text
nums = [-5, 2, -3, 4, -1]
```

There are three negative numbers, so the product is negative.

**Output:**
```text
-1
```

## Complexity Analysis

- **Time Complexity:** O(n) – Each array element is checked once.
- **Space Complexity:** O(1) – Only one extra variable is used.

## Key Learning

A product is negative when the array contains an odd number of negative elements, positive
