# LeetCode 2469 – Convert the Temperature

**Difficulty:** Easy  
**Language:** Java  
**Topic:** Basic Math, Variables, Arrays

## Problem
Given a temperature in Celsius, convert it into Kelvin and Fahrenheit. Return the results in an array where the first element is Kelvin and the second is Fahrenheit.

## Example

**Input**
```text
celsius = 36.50
```

**Output**
```text
[309.65000, 97.70000]
```

**Explanation**
- Kelvin = 36.50 + 273.15 = 309.65
- Fahrenheit = 36.50 × 1.80 + 32.00 = 97.70

## Java Solution

```java
class Solution {
    public double[] convertTemperature(double celsius) {
        double kelvin = celsius + 273.15;
        double fahrenheit = celsius * 1.80 + 32.00;

        return new double[]{kelvin, fahrenheit};
    }
}
```

## Logic
1. Receive the Celsius temperature.
2. Add `273.15` to calculate Kelvin.
3. Multiply Celsius by `1.80` and add `32.00` to calculate Fahrenheit.
4. Return both results in a `double[]` array.

## What I Learned
- Using `double` for decimal values.
- Performing arithmetic operations in Java.
- Returning multiple values using an array.
- Following the required method signature on LeetCode.

## Complexity Analysis
- **Time Complexity:** O(1)
- **Space Complexity:** O(1), excluding the returned array.

## Key Takeaway
This problem helped me practise Java variables, mathematical formulas, and returning arrays while solving an Easy LeetCode problem.

**Progress:** Daily LeetCode Practice 🚀