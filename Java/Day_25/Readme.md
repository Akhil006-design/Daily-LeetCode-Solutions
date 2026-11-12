# LeetCode 2108 – Find First Palindromic String in the Array

## Problem
Given an array of strings, return the first palindromic string. If no palindrome exists, return an empty string.

## Java Solution

```java
class Solution {
    public String firstPalindrome(String[] words) {
        for (int i = 0; i < words.length; i++) {
            String word = words[i];

            int left = 0;
            int right = word.length() - 1;

            boolean isPalindrome = true;

            while (left < right) {
                if (word.charAt(left) != word.charAt(right)) {
                    isPalindrome = false;
                    break;
                }

                left++;
                right--;
            }

            if (isPalindrome) {
                return word;
            }
        }

        return "";
    }
}
```

## Example

**Input:**
```text
["abc", "car", "ada", "racecar", "cool"]
```

**Output:**
```text
"ada"
```

## Approach
1. Traverse the array of words.
2. Use two pointers to compare the first and last characters.
3. Move both pointers towards the centre.
4. If every pair matches, return the word.
5. If no palindrome is found, return an empty string.

## Complexity Analysis
- **Time Complexity:** O(n × m), where n is the number of words and m is the maximum word length.
- **Space Complexity:** O(1) extra space.

## Key Learning
Character comparison, String operations, arrays, and the two-pointer technique.
