# LeetCode 1662 – Check If Two String Arrays are Equivalent

**Difficulty:** Easy  
**Language:** Java  
**Topic:** Strings, Arrays, For Loop

## Problem

Given two arrays of strings, check whether joining all the elements of both arrays produces the same string.

Return `true` if they are equal; otherwise, return `false`.

## Java Solution

```java
class Solution {
    public boolean arrayStringsAreEqual(String[] word1, String[] word2) {
        String str1 = "";
        String str2 = "";

        for (int i = 0; i < word1.length; i++) {
            str1 = str1 + word1[i];
        }

        for (int i = 0; i < word2.length; i++) {
            str2 = str2 + word2[i];
        }

        return str1.equals(str2);
    }
}
```

## Example

**Input:**
```text
word1 = ["ab", "c"]
word2 = ["a", "bc"]
```

**Output:**
```text
true
```

**Explanation:**

- First array becomes `"abc"`.
- Second array becomes `"abc"`.
- Both strings are equal, so the answer is `true`.

## Logic – Step by Step

1. Create two empty strings: `str1` and `str2`.
2. Use a `for` loop to join all elements of `word1`.
3. Use another `for` loop to join all elements of `word2`.
4. Use `.equals()` to compare both strings.
5. Return the result.

## Important Java Concepts

- `String[]` – stores multiple strings.
- `for` loop – accesses each array element.
- `.length` – gets the size of an array.
- `.equals()` – compares string contents.
- `return` – sends the result back.

## Time and Space Complexity

- **Time Complexity:** O(n + m), where n and m are the total character counts of both arrays.
- **Space Complexity:** O(n + m), for the combined strings.

## One-Line Logic

Join both string arrays and compare the resulting strings using `.equals()`.
