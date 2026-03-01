# Remove Duplicates from Sorted Array

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/remove-duplicates-from-sorted-array/submissions/1934531698/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def removeDuplicates(self, nums: List[int]) -> int:
        
        next = 1 # assign a variable to make the array ele shift to right as we keep scanning the next element is a duplicate or not

        for i in range(1, len(nums)): # we start looping from the 1st index, as if the array has one element that implies there are no duplicates
            if nums[i] != nums[i - 1]: # we check if the current ele is different from the prev ele or not
                nums[next] = nums[i] # if yes, we keep replacing to the next/right
                next += 1 # increment the right pointer
        
        return next # return the final count
```

---
*Generated automatically by LeetFeedback Extension*
