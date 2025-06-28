---
title: Fibonacci
date: 2025-06-28
author: Your Name
cell_count: 2
score: 0
---

```python
num = int(input("Enter number of terms to print in fibonacci series: "))
```

    Enter number of terms to print in fibonacci series:  8



```python
prevnum = 1
nextnum = 1
i = 1
print(prevnum, nextnum, end = ' ')
while i <= num - 2:
      number = prevnum+nextnum
      print(number, end = ' ')
      prevnum = nextnum
      nextnum = number
      i += 1
```

    1 1 2 3 5 8 13 21 


---
**Score: 0**