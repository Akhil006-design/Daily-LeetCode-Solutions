# LeetCode 2335 – Minimum Amount of Time to Fill Cups

**Difficulty:** Easy  
**Language:** Java

## Problem

You are given an array `amount` containing the number of cold, warm, and hot water cups.

In one second, you can fill either:
- One cup of any type.
- Two cups of different types.

Return the minimum number of seconds required to fill all cups.

## Java Solution

```java
class Solution {
    public int fillCups(int[] amount) {
        int max = 0;
        int sum = 0;

        for (int i = 0; i < amount.length; i++) {
            sum += amount[i];
            max = Math.max(max, amount[i]);
        }

        return Math.max(max, (sum + 1) / 2);
    }
}
```

## Algorithm

1. Initialize `max = 0` and `sum = 0`.
2. Traverse the array using a `for` loop.
3. Calculate the total number of cups.
4. Find the maximum number of cups of one type.
5. Calculate `(sum + 1) / 2`.
6. Return the maximum of `max` and `(sum + 1) / 2`.

## Example

**Input:**
```text
amount = [1, 4, 2]
```

**Working:**
```text
Total cups = 1 + 4 + 2 = 7
Maximum = 4

(sum + 1) / 2 = (7 + 1) / 2 = 4
```

**Output:**
```text
4
```

## Complexity Analysis

- **Time Complexity:** O(1), because the array always contains exactly three elements.
- **Space Complexity:** O(1), because only two extra variables are used.

## Key Concepts Learned

- Arrays
- For loop
- Maximum value using `Math.max()`
- Sum calculation
- Mathematical problem solving