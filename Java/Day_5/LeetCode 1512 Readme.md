# LeetCode 1512 — Number of Good Pairs

## 1. Problem

Given an integer array `nums`, find the number of good pairs.

A pair `(i, j)` is a good pair if:

- `nums[i] == nums[j]`
- `i < j`

In simple words, count how many pairs of elements have the same value, with the second element appearing later in the array.

## 2. Example

**Input:**
```text
nums = [1, 2, 3, 1, 1, 3]
```

**Output:**
```text
4
```

**Explanation:**

The good pairs are:

- `(0, 3)` because `nums[0] == nums[3]` → `1 == 1`
- `(0, 4)` because `nums[0] == nums[4]` → `1 == 1`
- `(2, 5)` because `nums[2] == nums[5]` → `3 == 3`
- `(3, 4)` because `nums[3] == nums[4]` → `1 == 1`

Total good pairs = `4`.

## 3. My Java Solution

```java
class Solution {
    public int numIdenticalPairs(int[] nums) {
        int count = 0;

        for (int i = 0; i < nums.length; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (nums[i] == nums[j]) {
                    count++;
                }
            }
        }

        return count;
    }
}
```

## 4. Logic

1. Initialize `count = 0`.
2. Use the outer `for` loop to select the first element.
3. Use the inner `for` loop to check elements after the first element.
4. Compare `nums[i]` and `nums[j]`.
5. If both values are equal, increase `count` by one.
6. Continue checking all possible pairs.
7. Return the final count.

## 5. What I Learned

- **Arrays:** Store multiple values of the same data type.
- **Array length:** `nums.length` gives the number of elements.
- **Nested loops:** A loop inside another loop helps check multiple pairs.
- **Array indexing:** `nums[i]` accesses an element at a particular index.
- **Comparison operator (`==`):** Checks whether two integer values are equal.
- **Increment operator (`count++`):** Increases a variable by one.
- **Return statement:** Returns the final answer from a method.

## 6. Understanding the Loops

For `nums = [1, 2, 3, 1, 1, 3]`:

| `i` | `j` | Comparison | Result |
|---:|---:|---|---|
| 0 | 1 | `1 == 2` | Not a good pair |
| 0 | 3 | `1 == 1` | Good pair, count = 1 |
| 0 | 4 | `1 == 1` | Good pair, count = 2 |
| 2 | 5 | `3 == 3` | Good pair, count = 3 |
| 3 | 4 | `1 == 1` | Good pair, count = 4 |

The algorithm checks every pair where `j > i` and counts matching values.

## 7. Why Does the Inner Loop Start at `i + 1`?

`for (int j = i + 1; j < nums.length; j++)`

This ensures that:

- An element is never paired with itself.
- The same pair is not counted twice.
- Only pairs satisfying `i < j` are checked.

## 8. Complexity Analysis

Let `n` be the number of elements in the array.

- **Time complexity:** `O(n²)` — nested loops check all possible pairs in the worst case.
- **Auxiliary space complexity:** `O(1)` — only a fixed number of extra variables are used.

## 9. My Key Takeaway

I learned how to use nested loops to compare array elements, identify matching pairs, and count them using a variable. I also understood why starting the inner loop at `i + 1` prevents duplicate pairs.

## 10. Possible Improvement

A frequency-counting approach can solve this problem in `O(n)` time by counting how many times each value appears and calculating how many new good pairs each occurrence creates.