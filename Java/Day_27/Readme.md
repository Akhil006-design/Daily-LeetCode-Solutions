# LeetCode 1704 – Determine if String Halves Are Alike

## Problem
Given a string of even length, divide it into two equal halves. Return true if both halves contain the same number of vowels. Otherwise, return false.

## Java Solution

```java
class Solution {
    public boolean halvesAreAlike(String s) {
        int count1 = 0;
        int count2 = 0;

        String vowels = "aeiouAEIOU";
        int half = s.length() / 2;

        for (int i = 0; i < half; i++) {
            if (vowels.indexOf(s.charAt(i)) != -1) {
                count1++;
            }

            if (vowels.indexOf(s.charAt(i + half)) != -1) {
                count2++;
            }
        }

        return count1 == count2;
    }
}
```

## Example

**Input:**
```text
"book"
```

**Output:**
```text
true
```

**Explanation:**
- First half: "bo" has 1 vowel.
- Second half: "ok" has 1 vowel.
- Both halves have the same number of vowels.

## Approach
1. Initialize two counters.
2. Store all vowels in a String.
3. Find the middle position.
4. Traverse both halves.
5. Count the vowels in each half.
6. Compare both counters and return the result.

## Complexity Analysis
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Key Learning
String traversal, character checking, indexOf(), and counting.
