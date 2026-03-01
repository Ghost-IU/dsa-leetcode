# Valid Anagram

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/valid-anagram/submissions/1934546595/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def isAnagram(self, s: str, t: str) -> bool:
        return sorted(s) == sorted(t)
```

---
*Generated automatically by LeetFeedback Extension*
