# Minimum Size Subarray Sum

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/minimum-size-subarray-sum/submissions/1934543397/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def minSubArrayLen(self, target: int, nums: List[int]) -> int:
        
        left = 0
        curSum = 0
        minLen = float('inf')

        for right in range(len(nums)):
            curSum += nums[right]
            while curSum >= target:
                minLen = min(minLen, right - left + 1)
                curSum -= nums[left]
                left += 1
        if minLen != float('inf'):
            return minLen
        else:
            return 0
```

---
*Generated automatically by LeetFeedback Extension*
