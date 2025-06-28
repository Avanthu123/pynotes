---
title: Lc2390-Removing-Stars-From-A-String
date: 2025-06-28
author: Your Name
cell_count: 3
score: 0
---

https://leetcode.com/problems/removing-stars-from-a-string/


```python
class Solution:
    def removeStars(self, s: str) -> str:
        nstar = []
        for i in s:
            if i == '*':
                nstar.pop()
            else:
                nstar.append(i)
        return ''.join(nstar)
```


```python
Solution().removeStars("leet**cod*e")
```




    'lecoe'




---
**Score: 0**