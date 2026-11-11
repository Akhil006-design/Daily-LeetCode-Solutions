# LeetCode 2000 – Reverse Prefix of Word

## Problem
Given a string `word` and a character `ch`, reverse the part of the string from the beginning up to and including the first occurrence of `ch`.

## Java Solution

```java
class Solution {
    public String reversePrefix(String word, char ch) {
        char[] arr = word.toCharArray();

        int index = word.indexOf(ch);

        if (index == -1) {
            return word;
        }

        int left = 0;
        int right = index;

        while (left < right) {
            char temp = arr[left];
            arr[left] = arr[right];
            arr[right] = temp;

            left++;
            right--;
        }

        return new String(arr);
    }
}
```

## Example

**Input:**
```text
word = "abcdefd", ch = "d"
```

**Output:**
```text
"dcbaefd"
```

## Approach
1. Convert the String into a character array.
2. Find the first occurrence of the given character.
3. Use two pointers to reverse the prefix.
4. Convert the character array back into a String.
5. Return the result.

## Complexity Analysis
- **Time Complexity:** O(n)
- **Space Complexity:** O(n)

## Key Learning
String operations, character arrays, two-pointer technique, and swapping.
