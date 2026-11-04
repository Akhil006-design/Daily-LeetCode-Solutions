# 104. Maximum Depth of Binary Tree

**Difficulty:** Easy  
**Topic:** Tree, Depth-First Search (DFS), Breadth-First Search (BFS), Binary Tree  
**Language:** Java *(or update based on your language)*

---

## Problem Statement

Given the `root` of a binary tree, return its maximum depth.

A binary tree's maximum depth is the number of nodes along the longest path from the root node down to the farthest leaf node.

### Example 1:

Input: root = [3,9,20,null,null,15,7]

### Example 2:

Input: root = [1,null,2]

## Approach & Explanation

### Approach 1: Recursive DFS (Depth-First Search)
The maximum depth of a binary tree is the maximum depth of its left subtree and right subtree, plus 1 (for the root node).

* **Base Case:** If the `root` is `null`, return `0`.
* **Recursive Step:** 
  $$\text{maxDepth}(\text{root}) = 1 + \max(\text{maxDepth}(\text{root.left}), \text{maxDepth}(\text{root.right}))$$

### Complexity Analysis
* **Time Complexity:** $O(N)$, where $N$ is the number of nodes in the tree. We visit each node exactly once.
* **Space Complexity:** $O(H)$, where $H$ is the height of the tree, due to the recursive call stack. In the worst case (skewed tree), it takes $O(N)$; in the best case (balanced tree), it takes $O(\log N)$.

---

