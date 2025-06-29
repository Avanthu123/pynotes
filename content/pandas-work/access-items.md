---
title: Access-Items
date: 2025-06-29
author: Your Name
cell_count: 11
score: 10
---

access-items


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
#acess a row
df.iloc[0]
```




    city      Toronto
    points         80
    Name: 0, dtype: object




```python
#access a column
df.iloc[:, 1]
```




    0    80
    1    70
    2    90
    Name: points, dtype: int64




```python
#acess an item
df.iloc[0, 1]
```




    np.int64(80)




```python
#acess acc to condition
df.loc[df['city'] == 'Waterloo']
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
      <th>2</th>
      <td>Waterloo</td>
      <td>90</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.loc[df['points'] > 70]
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
      <th>2</th>
      <td>Waterloo</td>
      <td>90</td>
    </tr>
  </tbody>
</table>
</div>




---
**Score: 10**