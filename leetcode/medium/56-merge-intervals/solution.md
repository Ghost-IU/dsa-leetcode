# Merge Intervals

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/merge-intervals/submissions/1934537390/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def merge(self, intervals: List[List[int]]) -> List[List[int]]:
        
        res = []

        intervals.sort(key=lambda x : x[0])

        current = intervals[0]

        for interval in intervals[1:]:
            if current[1] >= interval[0]:
                current[1] = max(current[1], interval[1])
            else:
                res.append(current)
                current = interval
            
        res.append(current)

        return res
```

---
*Generated automatically by LeetFeedback Extension*
