```python
import requests
from bs4 import BeautifulSoup

req = requests.get("https://klee313.github.io")
soup = BeautifulSoup(req.text, "html.parser")

article_url_a = soup.select('div.post-list-article > li > div > h3')
article_urls = []
for url in article_url_a:
    article_urls.append("https://klee313.github.io" + a.find("a").get("href"))
```