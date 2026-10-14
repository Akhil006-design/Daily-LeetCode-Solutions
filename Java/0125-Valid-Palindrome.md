# LeetCode 125 — Valid Palindrome

<<<<<<< HEAD
## 1. Problem
Check whether a string reads the same forward and backward, ignoring spaces, punctuation, and uppercase/lowercase differences.

## 2. Example
Input: "A man, a plan, a canal: Panama"
Output: true

## 3. What I Learned

- String: Stores a sequence of characters.
- toLowerCase(): Converts uppercase letters to lowercase.
- replaceAll(): Replaces text that matches a pattern.
- Two Pointers: Compares characters from opposite ends.
- charAt(): Gets a character at a particular index.
- while loop: Repeats instructions while a condition is true.
- Boolean: Represents true or false.

## 4. Logic

1. Remove punctuation and spaces.
2. Convert letters to lowercase.
3. Place one pointer at the beginning and one at the end.
4. Compare the characters at both pointers.
5. If they differ, return false.
6. Move both pointers toward the center.
7. If all comparisons match, return true.

## 5. Complexity

- Time: O(n)
- Space: O(n), because a cleaned string is created.

## 6. My Key Takeaway

I learned how to clean a string and use the two-pointer technique to check whether it is a palindrome.
=======
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
>>>>>>> 70fed1f3e1a416dbf1c59662ec557e07cc69ff2b
