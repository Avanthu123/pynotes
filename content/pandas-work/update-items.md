---
title: Update-Items
date: 2025-06-29
author: Your Name
cell_count: 9
score: 5
---

update-items


```python
import pandas as pd
```


```python
data = {
    'city' : ['Toronto', 'Montreal', 'Waterloo'],
    'points' : [80, 70, 90]
}
```


```python
data
```




    {'city': ['Toronto', 'Montreal', 'Waterloo'], 'points': [80, 70, 90]}




```python
df = pd.DataFrame(data)
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>city</th>
      <th>points</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toronto</td>
      <td>80</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Montreal</td>
      <td>70</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Waterloo</td>
      <td>90</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.loc[df['city'] == 'Montreal', 'points'] = 75
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>city</th>
      <th>points</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Toronto</td>
      <td>80</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Montreal</td>
      <td>75</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Waterloo</td>
      <td>90</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


---
**Score: 5**