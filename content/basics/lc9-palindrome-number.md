---
title: Lc9-Palindrome-Number
date: 2025-06-28
author: Your Name
cell_count: 5
score: 5
---

https://leetcode.com/problems/palindrome-number/


```python
class Solution:
    def isPalindrome(self, x: int) -> bool:
        pal, new = 0, x
        n = len(str(x))
        if x < 0:
            return False
        else:
            while n > 0:
                pal += (x % 10) * (10 ** (n-1))
                n -= 1
                x //= 10
            if pal == new:
                return True
            else:
                return False
```


```python
Solution().isPalindrome(1345431)
```




    True




```python
Solution().isPalindrome(-1)
```




    False




```python
Solution().isPalindrome(123)
```




    False




---
**Score: 5**