---
title: Factorial
date: 2025-06-29
author: Your Name
cell_count: 5
score: 5
---

```python
def factorial(num):
    if num < 0:
        return "Enter valid integer."
    fact = 1
    for i in range(1, num+1):
          fact *= i
    return fact
```


```python
factorial(7)
```




    5040




```python
factorial(0)
```




    1




```python
factorial(20)
```




    2432902008176640000




```python
factorial(-1)
```




    'Enter valid integer.'




---
**Score: 5**