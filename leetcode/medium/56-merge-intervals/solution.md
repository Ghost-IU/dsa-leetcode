# Merge Intervals

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/merge-intervals/submissions/1929961769/
- **Date:** 2026-02-24

## Solution

```python
class Solution:
    def merge(self, intervals: List[List[int]]) -> List[List[int]]:
        
        if not intervals:
            return []
        
        res = []

        intervals.sort(key= lambda x : x[0])

        current = intervals[0]

        for interval in intervals[1:]:
            if current[1] >= interval[0]:
                current[1] = max(interval[1], current[1])
            
            else:
                res.append(current)
                current = interval
            
        res.append(current)

        return res
```

---
*Generated automatically by LeetFeedback Extension*
