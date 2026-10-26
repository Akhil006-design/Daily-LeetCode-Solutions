# LeetCode 1365 – How Many Numbers Are Smaller Than the Current Number

**Difficulty:** Easy  
**Language:** Java  
**Topics:** Arrays, Nested Loops, Counting

## Problem Description

Given an integer array `nums`, return an array `answer` where `answer[i]` represents the number of elements in `nums` that are strictly smaller than `nums[i]`.

## Example

**Input**
```text
nums = [8, 1, 2, 2, 3]
```

**Output**
```text
[4, 0, 1, 1, 3]
```

**Explanation**

- `8` → Four numbers are smaller: `1, 2, 2, 3`.
- `1` → No numbers are smaller.
- `2` → One number is smaller: `1`.
- `2` → One number is smaller: `1`.
- `3` → Three numbers are smaller: `1, 2, 2`.

## Java Solution

```java
class Solution {
    public int[] smallerNumbersThanCurrent(int[] nums) {
        int[] answer = new int[nums.length];

        for (int i = 0; i < nums.length; i++) {
            int count = 0;

            for (int j = 0; j < nums.length; j++) {
                if (nums[j] < nums[i]) {
                    count++;
                }
            }

            answer[i] = count;
        }

        return answer;
    }
}
```

## Logic

1. Create an array to store the answers.
2. Select each number using the outer loop.
3. Compare it with every element using the inner loop.
4. If an element is smaller, increase the counter.
5. Store the counter in the corresponding answer position.
6. Return the answer array.

## Complexity Analysis

- **Time Complexity:** `O(n²)` – Each element is compared with every other element.
- **Space Complexity:** `O(n)` – An additional array stores the results.

## What I Learned

- Working with Java arrays.
- Using nested `for` loops.
- Applying `if` conditions to compare numbers.
- Counting elements that satisfy a condition.
- Storing results in a separate array.

## Key Takeaway

This problem helped me practise basic Java logic and nested loops by counting how many elements are smaller than each number.

**Progress:** Daily LeetCode Practice 🚀