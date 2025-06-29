---
title: Seaborn-Basics
date: 2025-06-29
author: Your Name
cell_count: 19
score: 15
---

```python
import pandas as pd
```


```python
import seaborn as sns
```


```python
data = pd.read_csv('student_scores.csv')
data
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
      <th>StudentID</th>
      <th>Math</th>
      <th>Science</th>
      <th>English</th>
      <th>History</th>
      <th>Geography</th>
      <th>ComputerScience</th>
      <th>Art</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>78</td>
      <td>85</td>
      <td>67</td>
      <td>72</td>
      <td>81</td>
      <td>88</td>
      <td>65</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>82</td>
      <td>78</td>
      <td>70</td>
      <td>75</td>
      <td>77</td>
      <td>92</td>
      <td>70</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>90</td>
      <td>92</td>
      <td>85</td>
      <td>88</td>
      <td>85</td>
      <td>95</td>
      <td>80</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>76</td>
      <td>88</td>
      <td>79</td>
      <td>74</td>
      <td>83</td>
      <td>87</td>
      <td>72</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>85</td>
      <td>82</td>
      <td>88</td>
      <td>79</td>
      <td>80</td>
      <td>90</td>
      <td>75</td>
    </tr>
  </tbody>
</table>
</div>




```python
data.plot()
```




    <Axes: >




    
![png](/pynotes/images/seaborn-basics_3_1.png)
    



```python
df = sns.load_dataset('tips')
df.head()
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
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>




```python
def category(row):
    x = row['total_bill']
    if x < 10:
        return 'low'
    elif x > 20:
        return 'high'
    else:
        return 'medium'
```


```python
df['category'] = df.apply(category, axis = 1)
df.head()
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
      <th>total_bill</th>
      <th>tip</th>
      <th>sex</th>
      <th>smoker</th>
      <th>day</th>
      <th>time</th>
      <th>size</th>
      <th>category</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>16.99</td>
      <td>1.01</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
      <td>medium</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10.34</td>
      <td>1.66</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
      <td>medium</td>
    </tr>
    <tr>
      <th>2</th>
      <td>21.01</td>
      <td>3.50</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>3</td>
      <td>high</td>
    </tr>
    <tr>
      <th>3</th>
      <td>23.68</td>
      <td>3.31</td>
      <td>Male</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>2</td>
      <td>high</td>
    </tr>
    <tr>
      <th>4</th>
      <td>24.59</td>
      <td>3.61</td>
      <td>Female</td>
      <td>No</td>
      <td>Sun</td>
      <td>Dinner</td>
      <td>4</td>
      <td>high</td>
    </tr>
  </tbody>
</table>
</div>




```python
#histogram
sns.histplot(data = df, x = 'total_bill')
```




    <Axes: xlabel='total_bill', ylabel='Count'>




    
![png](/pynotes/images/seaborn-basics_7_1.png)
    



```python
sns.histplot(data = df, x = 'total_bill', kde = True)
```




    <Axes: xlabel='total_bill', ylabel='Count'>




    
![png](/pynotes/images/seaborn-basics_8_1.png)
    



```python
sns.kdeplot(data = df, x = 'total_bill', hue = 'time', fill = True)
```




    <Axes: xlabel='total_bill', ylabel='Density'>




    
![png](/pynotes/images/seaborn-basics_9_1.png)
    



```python
sns.scatterplot(data = df, x = 'total_bill', y = 'tip')
```




    <Axes: xlabel='total_bill', ylabel='tip'>




    
![png](/pynotes/images/seaborn-basics_10_1.png)
    



```python
sns.scatterplot(data = df, x = 'total_bill', y = 'tip', hue = 'time')
```




    <Axes: xlabel='total_bill', ylabel='tip'>




    
![png](/pynotes/images/seaborn-basics_11_1.png)
    



```python
sns.lineplot(data = df, x = 'time', y = 'tip')
```




    <Axes: xlabel='time', ylabel='tip'>




    
![png](/pynotes/images/seaborn-basics_12_1.png)
    



```python
sns.barplot(data = df, x = 'day', y = 'tip')
```




    <Axes: xlabel='day', ylabel='tip'>




    
![png](/pynotes/images/seaborn-basics_13_1.png)
    



```python
sns.barplot(data = df, x = 'day', y = 'tip', hue = 'sex')
```




    <Axes: xlabel='day', ylabel='tip'>




    
![png](/pynotes/images/seaborn-basics_14_1.png)
    



```python
sns.boxplot(data=df, x= 'day', y='total_bill')
```




    <Axes: xlabel='day', ylabel='total_bill'>




    
![png](/pynotes/images/seaborn-basics_15_1.png)
    



```python
sns.violinplot(data = df, x = 'time', y = 'tip')
```




    <Axes: xlabel='time', ylabel='tip'>




    
![png](/pynotes/images/seaborn-basics_16_1.png)
    



```python
df1 = df.select_dtypes(include=['number'])
sns.heatmap(df1)
```




    <Axes: >




    
![png](/pynotes/images/seaborn-basics_17_1.png)
    



```python
sns.pairplot(df, hue = 'time')
```




    <seaborn.axisgrid.PairGrid at 0x7effbd50c190>




    
![png](/pynotes/images/seaborn-basics_18_1.png)
    



---
**Score: 15**