# LeetCode 1967 – Number of Strings That Appear as Substrings in Word

**Difficulty:** Easy

## Problem
Count how many strings in the patterns array appear as a substring inside the given word.

## Approach
1. Initialize count as 0.
2. Traverse the patterns array.
3. Check each pattern using `word.contains()`.
4. If the pattern exists, increase count.
5. Return count.

## Java Solution

```java
class Solution {
    public int numOfStrings(String[] patterns, String word) {
        int count = 0;

        for (int i = 0; i < patterns.length; i++) {
            if (word.contains(patterns[i])) {
                count++;
            }
        }

        return count;
    }
}
```

## Complexity
- Time Complexity: O(n × m × p) in the worst case.
- Space Complexity: O(1) extra space.

## Key Learning
- Java Strings
- contains() method
- Array traversal
- Counting matching elements