# Problem: Two Sum

**Difficulty**: Easy  
**Link**: [LeetCode - Two Sum](https://leetcode.com/problems/two-sum/)

## Problem Statement
Given an array of integers `nums` and an integer `target`, return the indices of the two numbers such that they add up to `target`.

### Constraints
- Each input would have exactly one solution.
- You may not use the same element twice.

### Example
**Input**: `nums = [2,7,11,15]`, `target = 9`  
**Output**: `[0, 1]`

---

## Solution (Python)
```python
def twoSum(nums, target):
    num_map = {}  # Dictionary to store numbers and their indices
    for i, num in enumerate(nums):
        complement = target - num
        if complement in num_map:
            return [num_map[complement], i]
        num_map[num] = i
