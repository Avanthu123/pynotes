---
title: Website-Scraping-Sample
date: 2025-06-29
author: Your Name
cell_count: 5
score: 5
---

```python
from bs4 import BeautifulSoup
import requests
```


```python
r = requests.get('https://en.wikipedia.org/wiki/2024_Indian_Premier_League')
```


```python
soup = BeautifulSoup(r.content, 'html.parser')
```


```python
tags = soup.find_all('h2')
for i in tags:
    print("\nArticle: ", i.text)
```

    
    Article:  Contents
    
    Article:  Background
    
    Article:  Teams
    
    Article:  Venues
    
    Article:  Opening ceremony
    
    Article:  League stage
    
    Article:  Playoffs
    
    Article:  Statistics and awards
    
    Article:  References
    
    Article:  External links



```python
tags = soup.find_all('h3')
for i in tags:
    print("\nArticle: ", i.text)
```

    
    Article:  Format
    
    Article:  Schedule
    
    Article:  Marketing
    
    Article:  Broadcasting
    
    Article:  Personnel changes
    
    Article:  Points table
    
    Article:  Match summary
    
    Article:  Fixtures
    
    Article:  Bracket
    
    Article:  Qualifier 1
    
    Article:  Eliminator
    
    Article:  Qualifier 2
    
    Article:  Final
    
    Article:  Most runs
    
    Article:  Most wickets
    
    Article:  Most Valuable Player
    
    Article:  End of season awards



---
**Score: 5**