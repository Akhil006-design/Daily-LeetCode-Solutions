# LeetCode 1678 — Goal Parser Interpretation

## Problem
Given a string `command`, interpret it using the following rules:
- `G` becomes `G`
- `()` becomes `o`
- `(al)` becomes `al`

Return the interpreted string.

## Example

**Input**
```text
command = "G()(al)"
```

**Output**
```text
"Goal"
```

**Explanation**

- `G` remains `G`
- `()` becomes `o`
- `(al)` becomes `al`

The final result is `Goal`.

## Java Solution

```java
class Solution {
    public String interpret(String command) {
        String result = "";

        for (int i = 0; i < command.length(); i++) {
            if (command.charAt(i) == 'G') {
                result += "G";
            } else if (command.charAt(i) == '(' && command.charAt(i + 1) == ')') {
                result += "o";
                i++;
            } else {
                result += "al";
                i += 3;
            }
        }

        return result;
    }
}
```

## Logic
1. Create an empty string called `result`.
2. Loop through the input command.
3. If the character is `G`, append `G`.
4. If the next two characters form `()`, append `o` and skip the closing parenthesis.
5. Otherwise, append `al` for `(al)` and skip the remaining characters.
6. Return the final result.

## Concepts Learned
- Java strings
- `charAt()` method
- `for` loops
- `if-else` conditions
- String concatenation

## Complexity Analysis
- **Time Complexity:** `O(n²)` for this implementation because repeated string concatenation can create new strings.
- **Space Complexity:** `O(n)` for the result, excluding temporary string allocations.

## Key Takeaway
Check each command and replace it according to the given rules to build the final interpreted string.
