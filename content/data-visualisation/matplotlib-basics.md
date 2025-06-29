---
title: Matplotlib-Basics
date: 2025-06-29
author: Your Name
cell_count: 13
score: 10
---

### Simple plot


```python
import pandas as pd
```


```python
import matplotlib.pyplot as plt
import numpy as np
```


```python
# A simple example
x = np.array([1, 2, 3, 4])
y = np.array([1, 2, 3, 4])
plt.plot(x, y)
plt.title('example')
plt.xlabel('x axis')
plt.ylabel('y axis')
plt.show()
```


    
![png](/pynotes/images/matplotlib-basics_3_0.png)
    


### Bar Graph


```python
df = pd.read_csv('student_scores.csv')
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
x = df.columns.tolist()[1:]
y = df.iloc[1, 1:]
plt.bar(x, y)
plt.xlabel('subjects')
plt.ylabel('marks')
plt.title('Scores of student 1')
plt.xticks(rotation=45)
plt.show()
```


    
![png](/pynotes/images/matplotlib-basics_6_0.png)
    


### Histogram


```python
plt.hist(df['Math'], bins = 10, edgecolor='black')
plt.xlabel('marks')
plt.ylabel('No. of students')
plt.title('Math marks')
plt.show()
```


    
![png](/pynotes/images/matplotlib-basics_8_0.png)
    


### Scatter Plot


```python
art = df['Art']
cs = df['ComputerScience']
plt.scatter(art, cs, marker = '*')
plt.xlabel('Art')
plt.ylabel('Computer Science')
plt.title('Scatter plot')
plt.grid()
plt.show()
```


    
![png](/pynotes/images/matplotlib-basics_10_0.png)
    


### Pie Chart

A graph in circular form that usually showcases a distribution or the percentage of different parts of a whole


```python
subjects = df.columns.tolist()[1:]
means = [df[sub].mean() for sub in subjects]

plt.figure(figsize=(8, 8))  # Adjust width and height as needed
plt.pie(means, labels=subjects, autopct='%1.1f%%')
plt.legend(loc='lower right')
plt.show()
```


    
![png](/pynotes/images/matplotlib-basics_12_0.png)
    



---
**Score: 10**