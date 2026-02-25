# Group Anagrams

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Medium
- **URL:** https://leetcode.com/problems/group-anagrams/submissions/1931040111/
- **Date:** 2026-02-25

## Solution

```python
class Solution:
    def groupAnagrams(self, strs: List[str]) -> List[List[str]]:
        
        anagram_map = defaultdict(list)

        for ele in strs:
            sorted_ele = "".join(sorted(ele))
            anagram_map[sorted_ele].append(ele)

        return list(anagram_map.values())
```

---
*Generated automatically by LeetFeedback Extension*
