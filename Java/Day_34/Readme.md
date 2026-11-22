# LeetCode 2037 – Minimum Number of Moves to Seat Everyone

**Difficulty:** Easy

## Problem
Find the minimum total number of moves required to place every student in a seat.

## Approach
1. Sort the seats array.
2. Sort the students array.
3. Match corresponding positions.
4. Calculate the absolute difference.
5. Add all differences and return the total.

## Java Solution

```java
import java.util.Arrays;

class Solution {
    public int minMovesToSeat(int[] seats, int[] students) {
        Arrays.sort(seats);
        Arrays.sort(students);

        int moves = 0;

        for (int i = 0; i < seats.length; i++) {
            moves += Math.abs(seats[i] - students[i]);
        }

        return moves;
    }
}
```

## Complexity
- Time Complexity: O(n log n)
- Auxiliary Space: Depends on sorting implementation.

## Key Learning
- Arrays.sort()
- For loop
- Math.abs()
- Array traversal
- Calculating minimum movement