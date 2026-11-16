# LeetCode 1523 – Count Odd Numbers in an Interval Range

## Problem
Given two integers `low` and `high`, return the number of odd numbers between them, including both endpoints.

## Java Solution

```java
class Solution {
    public int countOdds(int low, int high) {
        return (high + 1) / 2 - low / 2;
    }
}
```

## Example

**Input:**
```text
low = 3, high = 7
```

**Output:**
```text
3
```

**Explanation:** The odd numbers are 3, 5 and 7.

## Approach
1. Count the odd numbers from 1 to `high` using `(high + 1) / 2`.
2. Count the odd numbers before `low` using `low / 2`.
3. Subtract the second count from the first count.
4. Return the result.

## Complexity Analysis
- **Time Complexity:** O(1)
- **Space Complexity:** O(1)

## Key Learning
Java integer division, mathematical formulas, and method return values.
