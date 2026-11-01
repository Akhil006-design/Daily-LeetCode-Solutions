# LeetCode 1816 – Truncate Sentence

**Difficulty:** Easy  
**Language:** Java  
**Topics:** Strings, Arrays, For Loop, If Condition

## Problem

A sentence is given as a string `s` and an integer `k`.

Return the first `k` words of the sentence.

## Java Solution

```java
class Solution {
    public String truncateSentence(String s, int k) {
        String[] words = s.split(" ");
        String result = "";

        for (int i = 0; i < k; i++) {
            if (i > 0) {
                result = result + " ";
            }

            result = result + words[i];
        }

        return result;
    }
}
```

## Example

**Input:**
```text
s = "Hello how are you Contestant"
k = 4
```

**Output:**
```text
"Hello how are you"
```

## Logic – Step by Step

1. Use `split(" ")` to separate the sentence into individual words.
2. Store the words in a string array.
3. Create an empty string called `result`.
4. Run a loop from `0` to `k - 1`.
5. Add a space before every word except the first word.
6. Add each word to the result.
7. Return the final string.

## Important Java Concepts

- `split(" ")` – separates a sentence into words.
- `String[]` – stores multiple strings.
- `for` loop – accesses words one by one.
- `if` condition – checks whether a space is needed.
- `return` – returns the final answer.

## Complexity

- **Time Complexity:** O(n), where n is the sentence length.
- **Space Complexity:** O(n), for the words array and result.

## One-Line Logic

Split the sentence into words, take the first `k` words, and join them with spaces.
