# LeetCode 344 — Reverse String

## Problem

Write a function that reverses a character array in place using \(O(1)\) extra memory.

**Problem Link:** https://leetcode.com/problems/reverse-string/

## Example

**Input:**
```text
s = ['h', 'e', 'l', 'l', 'o']
```

**Output:**
```text
['o', 'l', 'l', 'e', 'h']
```

**Explanation:** The characters are reversed, so the first character becomes the last and the last becomes the first.

## Approach: Two Pointers

1. Create `left` at the beginning of the array.
2. Create `right` at the end of the array.
3. Swap the characters at both positions using a temporary variable.
4. Move `left` one step forward and `right` one step backward.
5. Repeat until `left` is no longer less than `right`.

## Java Solution

```java
class Solution {
    public void reverseString(char[] s) {
        int left = 0;
        int right = s.length - 1;

        while (left < right) {
            char temp = s[left];
            s[left] = s[right];
            s[right] = temp;

            left++;
            right--;
        }
    }
}
```

## Code Explanation

- `left = 0` points to the first character.
- `right = s.length - 1` points to the last character.
- `temp` temporarily stores a character during swapping.
- `left++` moves the left pointer forward.
- `right--` moves the right pointer backward.
- The loop stops when the pointers meet or cross.

## Complexity Analysis

- **Time Complexity:** `O(n)` — each character is processed at most once.
- **Space Complexity:** `O(1)` — only a constant amount of extra memory is used.

## What I Learned

- How to reverse an array in place.
- How to use the two-pointer technique.
- How to swap two characters using a temporary variable.
- How to solve a problem without creating another array.
