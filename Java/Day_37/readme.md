# LeetCode 557 – Reverse Words in a String III

**Difficulty:** Easy

## Problem
Reverse each word in a given sentence while keeping the original order of the words.

## Approach
1. Split the sentence into individual words.
2. Create an empty StringBuilder.
3. Traverse each word.
4. Reverse each word using `reverse()`.
5. Append the reversed word to the result.
6. Add spaces between words.
7. Return the final string.

## Java Solution

```java
class Solution {
    public String reverseWords(String s) {
        String[] words = s.split(" ");
        StringBuilder result = new StringBuilder();

        for (int i = 0; i < words.length; i++) {
            StringBuilder word = new StringBuilder(words[i]);

            result.append(word.reverse());

            if (i < words.length - 1) {
                result.append(" ");
            }
        }

        return result.toString();
    }
}
```

## Complexity
- Time Complexity: O(n)
- Space Complexity: O(n)

## Key Learning
- StringBuilder
- append()
- reverse()
- toString()
- String split()