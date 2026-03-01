# Rotate Array

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/rotate-array/submissions/1934533092/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def rotate(self, nums: List[int], k: int) -> None:
        """
        Do not return anything, modify nums in-place instead.
        """
        k = k % len(nums)

        nums[:] = nums[-k:] + nums[:-k]
```

---
*Generated automatically by LeetFeedback Extension*
