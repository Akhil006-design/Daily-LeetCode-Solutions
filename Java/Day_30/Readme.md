# LeetCode 1460 – Make Two Arrays Equal by Reversing Subarrays

## Problem
Given two integer arrays `target` and `arr`, return true if `arr` can be made equal to `target` by reversing subarrays any number of times.

## Java Solution

```java
import java.util.Arrays;

class Solution {
    public boolean canBeEqual(int[] target, int[] arr) {
        Arrays.sort(target);
        Arrays.sort(arr);

        return Arrays.equals(target, arr);
    }
}
```

## Example

**Input:**
```text
target = [1, 2, 3, 4]
arr = [2, 4, 1, 3]
```

**Output:**
```text
true
```

**Explanation:** After sorting, both arrays become `[1, 2, 3, 4]`.

## Approach
1. Sort the target array.
2. Sort the given array.
3. Compare both arrays using `Arrays.equals()`.
4. Return the comparison result.

## Complexity Analysis
- **Time Complexity:** O(n log n)
- **Space Complexity:** Depends on the sorting implementation.

## Key Learning
Array sorting, array comparison, and the Arrays utility class.
