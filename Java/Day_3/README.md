# LeetCode 1281 — Subtract the Product and Sum of Digits of an Integer

## 1. Problem

Given an integer `n`, calculate the product of its digits and the sum of its digits. Return the product minus the sum.

## 2. Example

**Input:** `n = 234`

- Product = 2 × 3 × 4 = 24
- Sum = 2 + 3 + 4 = 9
- Result = 24 − 9 = 15

**Output:** `15`

## 3. What I Learned

### 1. Variables

Variables store values that change while the program runs.

- `product = 1`: Stores the multiplication result.
- `sum = 0`: Stores the addition result.
- `digit`: Stores the current digit extracted from `n`.

**Important:** Product starts at `1` because multiplying by `1` does not change the result. Sum starts at `0` because adding `0` does not change the result.

### 2. While Loop

`while (n > 0)` repeats the code as long as `n` is greater than zero.

It helps process every digit until no digits remain.

### 3. Modulo Operator (`%`)

`int digit = n % 10;`

The `%` operator gives the remainder. For a positive integer, `n % 10` extracts its last digit.

Example: `234 % 10 = 4`.

### 4. Integer Division (`/`)

`n = n / 10;`

Integer division removes the last digit from a positive integer.

Example: `234 / 10 = 23`.

### 5. Multiplication and Addition

- `product = product * digit;` multiplies the extracted digit into the product.
- `sum = sum + digit;` adds the extracted digit to the sum.

### 6. Return Statement

`return product - sum;`

Returns the difference between the product and the sum of the digits.

## 4. How the Code Works

For `n = 234`:

| Step | Digit (`n % 10`) | Product | Sum | Remaining `n` |
|---|---:|---:|---:|---:|
| 1 | 4 | 4 | 4 | 23 |
| 2 | 3 | 12 | 7 | 2 |
| 3 | 2 | 24 | 9 | 0 |

Final answer: `24 - 9 = 15`.

## 5. Algorithm

1. Initialize `product = 1` and `sum = 0`.
2. Repeat while `n > 0`.
3. Extract the last digit using `n % 10`.
4. Multiply the digit into `product`.
5. Add the digit to `sum`.
6. Remove the last digit using `n / 10`.
7. Return `product - sum`.

## 6. Complexity

Let `d` be the number of digits in `n`.

- **Time complexity:** O(d), because each digit is processed once.
- **Auxiliary space complexity:** O(1), because only a fixed number of variables are used.

## 7. My Key Takeaway

I learned how to extract digits using modulo, remove digits using integer division, repeat operations with a while loop, and calculate the product and sum of an integer's digits.