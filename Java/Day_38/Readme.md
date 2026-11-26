# LeetCode 867 – Transpose Matrix

**Difficulty:** Easy

## Problem
Given a matrix, return its transpose by converting rows into columns and columns into rows.

## Approach
1. Find the number of rows and columns.
2. Create a new matrix with reversed dimensions.
3. Traverse the original matrix using nested loops.
4. Store each element at the swapped position.
5. Return the new matrix.

## Java Solution

```java
class Solution {
    public int[][] transpose(int[][] matrix) {
        int rows = matrix.length;
        int cols = matrix[0].length;

        int[][] result = new int[cols][rows];

        for (int i = 0; i < rows; i++) {
            for (int j = 0; j < cols; j++) {
                result[j][i] = matrix[i][j];
            }
        }

        return result;
    }
}
```

## Complexity
- Time Complexity: O(rows × cols)
- Space Complexity: O(rows × cols)

## Key Learning
- 2D Arrays
- Rows and Columns
- Nested Loops
- Matrix Transpose