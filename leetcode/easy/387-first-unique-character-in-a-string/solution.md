# First Unique Character in a String

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/first-unique-character-in-a-string/submissions/1934576354/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def firstUniqChar(self, s: str) -> int:
        hashmap = {}

        for ele in s:
            hashmap[ele] = hashmap.get(ele, 0) + 1 # looping through all the elements and capturing and storing its freq

        for i in range(len(s)):
            if hashmap[s[i]] == 1: # check the element with freq of 1
                return i
        
        return -1

```

---
*Generated automatically by LeetFeedback Extension*
