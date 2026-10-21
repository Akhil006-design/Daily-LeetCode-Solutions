# LeetCode 1929 — Concatenation of Array

## 1. Problem

Given an integer array `nums` of length `n`, create a new array `ans` of length `2n` such that the first `n` elements of `ans` are the same as `nums`, and the next `n` elements are also the same as `nums`.

In simple words, repeat the original array twice.

## 2. Example

**Input:**
```text
nums = [1, 2, 1]
```

**Output:**
```text
[1, 2, 1, 1, 2, 1]
```

**Explanation:**

The original array `[1, 2, 1]` is repeated twice to produce `[1, 2, 1, 1, 2, 1]`.

## 3. My Java Solution

```java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int n = nums.length;

        int[] ans = new int[2 * n];

        for (int i = 0; i < n; i++) {
            ans[i] = nums[i];
            ans[i + n] = nums[i];
        }

        return ans;
    }
}
```

## 4. Logic

1. Store the length of the original array in `n`.
2. Create a new array with twice the original length.
3. Use a `for` loop to visit each element of `nums`.
4. Copy each element to position `i` in the new array.
5. Copy the same element to position `i + n`.
6. Return the completed array.

## 5. What I Learned

- **Arrays:** Store multiple values of the same data type.
- **Array length:** `nums.length` gives the number of elements.
- **Array creation:** `new int[2 * n]` creates an integer array with twice the original length.
- **For loop:** Repeats instructions for each array element.
- **Array indexing:** `ans[i]` accesses a position in the new array.
- **Index calculation:** `i + n` identifies the corresponding position in the second half.
- **Return statement:** Returns the completed array to the caller.

## 6. Understanding the Loop

For `nums = [1, 2, 1]`, the length is `n = 3`.

| `i` | `ans[i]` | `ans[i + n]` |
|---:|---|---|
| 0 | `ans[0] = 1` | `ans[3] = 1` |
| 1 | `ans[1] = 2` | `ans[4] = 2` |
| 2 | `ans[2] = 1` | `ans[5] = 1` |

The final array is `[1, 2, 1, 1, 2, 1]`.

## 7. Complexity Analysis

- **Time Complexity:** `O(n)` — the loop processes each element once, performing a constant amount of work per iteration.
- **Auxiliary Space Complexity:** `O(n)` — a new array of length `2n` is created.

## 8. My Key Takeaway

I learned how to create a new array, use a loop to copy elements, and calculate array indices to repeat an array twice.