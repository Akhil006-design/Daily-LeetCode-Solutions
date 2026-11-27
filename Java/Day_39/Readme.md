# LeetCode 1051 – Height Checker

**Difficulty:** Easy

## Problem
Count how many students are not standing in their expected height order.

## Approach
1. Copy the original heights array.
2. Sort the copied array.
3. Compare both arrays element by element.
4. Increase count whenever the elements differ.
5. Return the count.

## Java Solution

```java
import java.util.Arrays;

class Solution {
    public int heightChecker(int[] heights) {
        int[] expected = heights.clone();

        Arrays.sort(expected);

        int count = 0;

        for (int i = 0; i < heights.length; i++) {
            if (heights[i] != expected[i]) {
                count++;
            }
        }

        return count;
    }
}
```

## Complexity
- Time Complexity: O(n log n)
- Space Complexity: O(n)

## Key Learning
- Array cloning
- Arrays.sort()
- Array comparison
- Counting mismatched elements