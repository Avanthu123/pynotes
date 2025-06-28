---
title: Website-Scraping-Sample
date: 2025-06-28
author: Your Name
cell_count: 1
score: 0
---

```python
from bs4 import BeautifulSoup
import requests

r = requests.get('https://en.wikipedia.org/wiki/2024_Indian_Premier_League')

soup = BeautifulSoup(r.content, 'html.parser')

tags = soup.find_all('h2')
for i in tags:
    print("\nArticle: ", i.text)
```


---
**Score: 0**