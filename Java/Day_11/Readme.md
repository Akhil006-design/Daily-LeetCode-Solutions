# LeetCode 1614 – Maximum Nesting Depth of the Parentheses

**Difficulty:** Easy  
**Language:** Java  
**Topics:** Strings, Loops, Conditional Statements

## Problem Description

Given a valid parentheses string `s`, return the maximum nesting depth of the parentheses.

The nesting depth is the maximum number of opening parentheses that are waiting to be closed at any point in the string.

## Example

**Input**
```text
s = "(1+(2*3)+((8)/4))+1"
```

**Output**
```text
3
```

**Explanation**

The deepest part of the expression contains three nested opening parentheses. Therefore, the maximum nesting depth is `3`.

## Java Solution

```java
class Solution {
    public int maxDepth(String s) {
        int depth = 0;
        int maxDepth = 0;

        for (int i = 0; i < s.length(); i++) {
            if (s.charAt(i) == '(') {
                depth++;

                if (depth > maxDepth) {
                    maxDepth = depth;
                }
            } else if (s.charAt(i) == ')') {
                depth--;
            }
        }

        return maxDepth;
    }
}
```

## Logic

1. Initialize `depth` and `maxDepth` to `0`.
2. Traverse each character in the string.
3. If the character is `'('`, increase `depth`.
4. Update `maxDepth` if the current depth is greater.
5. If the character is `')'`, decrease `depth`.
6. Return `maxDepth`.

## Complexity Analysis

- **Time Complexity:** `O(n)` – Each character is visited once.
- **Space Complexity:** `O(1)` – Only two integer variables are used.

## What I Learned

- Accessing characters in a Java string using `charAt()`.
- Using `for` loops to traverse strings.
- Applying `if/else if` conditions.
- Tracking a current value and its maximum.

## Key Takeaway

This problem helped me practise Java strings, loops, and conditional statements by tracking the nesting depth of parentheses.

**Progress:** Daily LeetCode Practice 🚀