# LeetCode 2119 – A Number After a Double Reversal

**Difficulty:** Easy  
**Language:** Java

## Problem

Given an integer `num`, reverse its digits twice.

Return `true` if the final number is equal to the original number. Otherwise, return `false`.

## Java Solution

```java
class Solution {
    public boolean isSameAfterReversals(int num) {
        int original = num;
        int reversed = 0;

        while (num > 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num = num / 10;
        }

        num = reversed;
        reversed = 0;

        while (num > 0) {
            int digit = num % 10;
            reversed = reversed * 10 + digit;
            num = num / 10;
        }

        return original == reversed;
    }
}
```

## Algorithm

1. Store the original number in `original`.
2. Initialize `reversed = 0`.
3. Extract the last digit using `num % 10`.
4. Add the digit to the reversed number.
5. Remove the last digit using `num / 10`.
6. Repeat until the number becomes zero.
7. Reverse the first reversed number again.
8. Compare the final number with the original.
9. Return the comparison result.

## Example 1

**Input:**
```text
num = 526
```

**Working:**
```text
First reversal: 625
Second reversal: 526
```

**Output:**
```text
true
```

## Example 2

**Input:**
```text
num = 1800
```

**Working:**
```text
First reversal: 81
Second reversal: 18
```

**Output:**
```text
false
```

## Complexity Analysis

- **Time Complexity:** O(d), where d is the number of digits. Two reversals each take O(d) time.
- **Space Complexity:** O(1), because only a fixed number of variables are used.

## Key Concepts Learned

- `while` loops
- Modulo operator (`%`)
- Integer division (`/`)
- Number reversal
- Boolean return values
