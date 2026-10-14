# LeetCode 125 — Valid Palindrome

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
