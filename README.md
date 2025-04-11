# 🧮 Count Symmetric Integers - LeetCode #2843

This repository contains a Python solution for LeetCode Problem **2843: Count Symmetric Integers**. The problem is categorized as *Easy* and focuses on checking numeric symmetry based on digit sums.

## 📌 Problem Statement

Given two positive integers `low` and `high`, return the number of **symmetric integers** between them.

A symmetric integer has an even number of digits and the **sum of the first half of the digits equals the sum of the second half**.

### 🔍 Examples

**Example 1:**
#### Input: 
low = 1, 
high = 100
#### Output:
9
#### Explanation: 
11, 22, 33, ..., 99 are symmetric.

---

## 🚀 Solution

The solution is implemented in Python using a helper function that:

1. Converts the number to a string.
2. Ensures the number has even digits.
3. Splits it in half and compares the sum of the two halves.

### 🧠 Core Code:

```python
class Solution(object):
    def countSymmetricIntegers(self, low, high):
        def is_symmetric(num):
            s = str(num)
            if len(s) % 2 != 0:
                return False
            mid = len(s) // 2
            return sum(int(d) for d in s[:mid]) == sum(int(d) for d in s[mid:])
        
        return sum(1 for num in range(low, high + 1) if is_symmetric(num))
```
# 📺 From Coding Moves
This solution is part of the Coding Moves series, where I solve coding problems and share programming content to help learners grow.

+ 📌 Follow my journey:

+ 🌐 YouTube: <a href="https://www.youtube.com/@Coding_Moves">Coding Moves</a>

+ 🧠 Projects | DSA | Python | AI | Math

