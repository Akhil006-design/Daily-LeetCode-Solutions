# LeetCode 125 — Valid Palindrome

## Problem
Check whether a string reads the same forward and backward, ignoring punctuation, spaces, and uppercase/lowercase differences.

## Example
**Input:** `"A man, a plan, a canal: Panama"`

**Output:** `true`

## What I Learned

1. **Strings:** A sequence of characters.
2. **`toLowerCase()`:** Converts uppercase letters to lowercase.
3. **`replaceAll()`:** Removes unwanted characters using a pattern.
4. **Two Pointers:** Compare characters from the beginning and end.
5. **`charAt()`:** Gets a character at a particular index.
6. **`while` Loop:** Repeats comparisons until the pointers meet.
7. **Boolean:** Returns `true` or `false`.

## Logic

1. Remove punctuation and spaces.
2. Convert all letters to lowercase.
3. Set one pointer at the beginning and another at the end.
4. Compare both characters.
5. If they differ, return `false`.
6. Move the pointers toward each other.
7. If all characters match, return `true`.

## Complexity

- **Time:** O(n)
- **Space:** O(n), because a cleaned string is created.

## My Key Takeaway

I learned how to process strings and use the two
