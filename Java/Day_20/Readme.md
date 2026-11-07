# LeetCode 2535 – Difference Between Element Sum and Digit Sum of an Array

**Difficulty:** Easy  
**Language:** Java

## Problem

Given an integer array `nums`, calculate the difference between:

- Element Sum: Sum of all elements in the array.
- Digit Sum: Sum of every individual digit in the array.

Return the absolute difference between these two sums.

## Java Solution

```java
class Solution {
    public int differenceOfSum(int[] nums) {
        int elementSum = 0;
        int digitSum = 0;

        for (int i = 0; i < nums.length; i++) {
            elementSum += nums[i];

            int temp = nums[i];

            while (temp > 0) {
                int digit = temp % 10;
                digitSum += digit;
                temp = temp / 10;
            }
        }

        return Math.abs(elementSum - digitSum);
    }
}
```

## Algorithm

1. Initialize `elementSum` and `digitSum` to zero.
2. Traverse the array using a `for` loop.
3. Add each element to `elementSum`.
4. Store the current element in a temporary variable.
5. Extract each digit using `% 10`.
6. Add each digit to `digitSum`.
7. Remove the last digit using `/ 10`.
8. Return `Math.abs(elementSum - digitSum)`.

## Example

**Input:**
```text
nums = [1, 15, 6, 3]
```

**Element Sum:**
```text
1 + 15 + 6 + 3 = 25
```

**Digit Sum:**
```text
1 + 1 + 5 + 6 + 3 = 16
```

**Output:**
```text
9
```

## Complexity Analysis

- **Time Complexity:** O(n × d), where n is the number of array elements and d is the maximum number of digits in an element.
- **Space Complexity:** O(1), because only a fixed number of variables are used.

## Key Concepts Learned

- `for` loop
- `while` loop
- Arrays
- Modulo operator (`%`)
- Integer division (`/`)
- `Math.abs()` method