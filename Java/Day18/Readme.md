class Solution {
    public int countDigits(int num) {
        int sum = 0;
        int temp = num;

        while (temp > 0) {
            int digit = temp % 10;

            if (num % digit == 0) {
                sum++;
            }

            temp = temp / 10;
        }

        return sum;
    }
}# LeetCode 2520 – Count the Digits That Divide a Number

**Difficulty:** Easy  
**Language:** Java

## Problem

Given an integer `num`, count how many digits in the number divide the original number without leaving a remainder.

## Java Solution

```java
class Solution {
    public int countDigits(int num) {
        int sum = 0;
        int temp = num;

        while (temp > 0) {
            int digit = temp % 10;

            if (num % digit == 0) {
                sum++;
            }

            temp = temp / 10;
        }

        return sum;
    }
}
```

## Logic – Step by Step

1. Initialize `sum = 0` to count the digits.
2. Store the original number in `temp`.
3. Extract the last digit using `temp % 10`.
4. Check whether the original number is divisible by that digit using `num % digit == 0`.
5. If divisible, increase `sum`.
6. Remove the last digit using `temp / 10`.
7. Repeat until `temp` becomes zero.
8. Return `sum`.

## Example

**Input:**
```text
num = 1248
```

| Digit | Divisibility check | Result |
|---|---|---|
| 8 | 1248 % 8 | Divisible |
| 4 | 1248 % 4 | Divisible |
| 2 | 1248 % 2 | Divisible |
| 1 | 1248 % 1 | Divisible |

**Output:**
```text
4
```

## Complexity Analysis

- **Time Complexity:** O(d), where d is the number of digits.
- **Space Complexity:** O(1), because only a fixed number of variables are used.

## Key Concepts Learned

- `while` loop
- Modulo operator (`%`)
- Integer division (`/`)
- Extracting digits from a number
- Conditional statements (`if`)