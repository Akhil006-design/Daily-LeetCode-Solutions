# LeetCode 1832 – Check if the Sentence Is Pangram

## Problem
A pangram is a sentence that contains every English alphabet letter at least once.

Return `true` if the sentence contains all 26 letters. Otherwise, return `false`.

## Java Solution

```java
class Solution {
    public boolean checkIfPangram(String sentence) {
        boolean[] seen = new boolean[26];

        for (int i = 0; i < sentence.length(); i++) {
            int index = sentence.charAt(i) - 'a';
            seen[index] = true;
        }

        for (int i = 0; i < 26; i++) {
            if (!seen[i]) {
                return false;
            }
        }

        return true;
    }
}
```

## Example

**Input:**
```text
"thequickbrownfoxjumpsoverthelazydog"
```

**Output:**
```text
true
```

## Approach
1. Create a Boolean array of size 26.
2. Traverse every character in the sentence.
3. Convert each character into an alphabet index using `character - 'a'`.
4. Mark the corresponding index as true.
5. Check whether all 26 positions are true.
6. Return the result.

## Complexity Analysis
- **Time Complexity:** O(n)
- **Space Complexity:** O(1), because the Boolean array always has 26 elements.

## Key Learning
String traversal, character indexing, Boolean arrays, and checking whether all elements are present.
