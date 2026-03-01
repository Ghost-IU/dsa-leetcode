# Maximum Subarray

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/maximum-subarray/submissions/1934526970/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def maxSubArray(self, nums: List[int]) -> int:
        
        curSum = 0
        maxSum = -inf

        for num in nums:

            curSum += num

            if curSum > maxSum:
                maxSum = curSum
            
            if curSum < 0:
                curSum = 0
        
        return maxSum
```

---
*Generated automatically by LeetFeedback Extension*
