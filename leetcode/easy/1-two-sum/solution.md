# Two Sum

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/two-sum/submissions/1934525317/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        
        hashmap =  {}

        for i in range(len(nums)):
            hashmap[nums[i]] = i
        
        for i in range(len(nums)):
            comp = target - nums[i]

            if comp in hashmap and hashmap[comp] != i:
                return [i, hashmap[comp]]
        
        return []
```

---
*Generated automatically by LeetFeedback Extension*
