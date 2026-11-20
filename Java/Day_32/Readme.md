# LeetCode 1491 – Average Salary Excluding the Minimum and Maximum Salary

**Difficulty:** Easy

## Problem
Calculate the average salary after excluding the minimum and maximum salaries from the given array.

## Approach
1. Calculate the total sum.
2. Find the minimum and maximum values.
3. Subtract them from the total.
4. Divide by the remaining number of elements.

## Java Solution

```java
class Solution {
    public double average(int[] salary) {
        int sum = 0;
        int min = salary[0];
        int max = salary[0];

        for (int i = 0; i < salary.length; i++) {
            sum += salary[i];
            min = Math.min(min, salary[i]);
            max = Math.max(max, salary[i]);
        }

        return (double) (sum - min - max) / (salary.length - 2);
    }
}
```

## Complexity
- Time Complexity: O(n)
- Space Complexity: O(1)

## Key Learning
- Math.min()
- Math.max()
- Array traversal
- Calculating averages using double