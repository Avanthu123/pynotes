---
title: Lc7-Reverse-Integer
date: 2025-06-29
author: Your Name
cell_count: 5
score: 5
---

https://leetcode.com/problems/reverse-integer/


```python
class Solution:
    def reverse(self, x: int) -> int:
        sign = -1 if x<0 else 1
        x*= sign
        y = 0
        while x:
            y = y*10+x%10
            x = x//10
        if sign == -1:
            y*= sign
        if y < -2**31 or y > 2**31 - 1:
            return 0
        return y
```


```python
Solution().reverse(1827386)
```




    6837281




```python
Solution().reverse(-1272)
```




    -2721




```python
Solution().reverse(2**32)
```




    0




---
**Score: 5**