# LeetCode 1290 – Convert Binary Number in a Linked List to Integer

## Problem
Given a linked list containing binary digits (0 and 1), convert the binary number into its decimal integer value.

## Java Solution

```java
class Solution {
    public int getDecimalValue(ListNode head) {
        int result = 0;

        while (head != null) {
            result = result * 2 + head.val;
            head = head.next;
        }

        return result;
    }
}
```

## Example

**Input:**
```text
1 -> 0 -> 1
```

**Output:**
```text
5
```

**Explanation:**

Binary 101 = Decimal 5.

## Approach
1. Initialize result as 0.
2. Traverse the linked list.
3. Multiply the current result by 2.
4. Add the current node value.
5. Move to the next node.
6. Return the final result.

## Complexity Analysis
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Key Learning
Linked list traversal, binary-to-decimal conversion, and mathematical operations.
