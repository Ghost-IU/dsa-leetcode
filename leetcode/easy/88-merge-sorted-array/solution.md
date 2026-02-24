# Merge Sorted Array

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/merge-sorted-array/submissions/1929948264/
- **Date:** 2026-02-24

## Solution

```python
class Solution:
    def merge(self, nums1: List[int], m: int, nums2: List[int], n: int) -> None:
        """
        Do not return anything, modify nums1 in-place instead.
        """
        nums1[:] = sorted(nums1[:m] + nums2)
```

---
*Generated automatically by LeetFeedback Extension*
