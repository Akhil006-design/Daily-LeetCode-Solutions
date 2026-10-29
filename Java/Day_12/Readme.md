# LeetCode 1528 – Shuffle String

## Problem Description
Given a string `s` and an integer array `indices` of the same length, rearrange the characters of the string so that the character at position `i` moves to position `indices[i]`.

Return the restored string.

## Java Solution

```java
class Solution {
    public String restoreString(String s, int[] indices) {
        char[] result = new char[s.length()];

        for (int i = 0; i < s.length(); i++) {
            result[indices[i]] = s.charAt(i);
        }

        return new String(result);
    }
}
```

## Example

**Input:**
```text
s = "codeleet"
indices = [4,5,6,7,0,2,1,3]
```

**Output:**
```text
"leetcode"
```

## Approach

1. Create a character array named `result` with the same length as the input string.
2. Use a `for` loop to visit every character in the string.
3. Place each character at the position specified by `indices[i]`.
4. Convert the character array into a string and return it.

## Complexity Analysis

- **Time Complexity:** O(n), because each character is processed once.
- **Space Complexity:** O(n), because a new character array is created.

## Key Learning

Learned how to use `charAt()`, character arrays, and array indices to rearrange a string in Java.
