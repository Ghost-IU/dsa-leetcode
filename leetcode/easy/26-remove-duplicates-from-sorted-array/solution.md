# Remove Duplicates from Sorted Array

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/remove-duplicates-from-sorted-array/submissions/1934529887/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        
        next = 1

        for i in range(1, len(nums)):
            if nums[i] != nums[i - 1]:
                nums[next] = nums[i]
                next += 1
        
        return next
```

---
*Generated automatically by LeetFeedback Extension*
