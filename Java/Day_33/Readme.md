# LeetCode 2089 – Find Target Indices After Sorting Array

**Difficulty:** Easy

## Problem
Sort the given array and return all indices where the target element appears.

## Approach
1. Sort the array.
2. Create an empty ArrayList.
3. Traverse the sorted array.
4. If an element matches the target, add its index.
5. Return the list.

## Java Solution

```java
import java.util.*;

class Solution {
    public List<Integer> targetIndices(int[] nums, int target) {
        Arrays.sort(nums);

        List<Integer> result = new ArrayList<>();

        for (int i = 0; i < nums.length; i++) {
            if (nums[i] == target) {
                result.add(i);
            }
        }

        return result;
    }
}
```

## Complexity
- Time Complexity: O(n log n)
- Space Complexity: O(n) for the result list

## Key Learning
- Linear search
- Arrays.sort()
- ArrayList
- Finding multiple matching indices