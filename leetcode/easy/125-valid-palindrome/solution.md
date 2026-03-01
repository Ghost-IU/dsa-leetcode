# Valid Palindrome

## Problem Information
- **Platform:** Leetcode
- **Difficulty:** Easy
- **URL:** https://leetcode.com/problems/valid-palindrome/submissions/1934562431/
- **Date:** 2026-03-01

## Solution

```python
class Solution:
    def isPalindrome(self, s: str) -> bool:
        
        s = "".join(char.lower() for char in s if char.isalnum())
        return s[::-1] == s
```

---
*Generated automatically by LeetFeedback Extension*
