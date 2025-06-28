---
title: Lc4-Median-Of-Two-Sorted-Arrays
date: 2025-06-28
author: Your Name
cell_count: 6
score: 5
---

https://leetcode.com/problems/median-of-two-sorted-arrays/


```python
class Solution:
    def findMedianSortedArrays(self, nums1: list[int], nums2: list[int]) -> float:
        arr = nums1+nums2
        arr.sort()
        n = len(arr)
        if n%2 == 0:
            median = (arr[n//2]+arr[(n//2)-1])/2
        else:
            median = arr[n//2]
        return median
```


```python
Solution().findMedianSortedArrays(nums1 = [1,1,2,4,6,8,9,11], nums2 = [3,4,9,13,17,19,21])
```




    8




```python
Solution().findMedianSortedArrays(nums1 = [1,9,11], nums2 = [3,4,21])
```




    6.5




```python
Solution().findMedianSortedArrays(nums1 = [1], nums2 = [3])
```




    2.0




```python
Solution().findMedianSortedArrays(nums1 = [1], nums2 = [])
```




    1




---
**Score: 5**