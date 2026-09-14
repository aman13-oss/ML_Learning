# Day 18 – Pandas DataFrame Using Web Scraping

## 📌 What I Learned

In Day 18, I learned how to **scrape data from a website using Python** and convert that scraped data into a **Pandas DataFrame**.

For practice, instead of AmbitionBox, I used **Books to Scrape**, which allowed me to practice the same web-scraping concepts on a larger dataset.

---

## 🛠️ Libraries Used

```python
import pandas as pd
import requests
from bs4 import BeautifulSoup
import numpy as np
```

### Libraries

* **Requests** → Website se HTML page fetch karne ke liye
* **BeautifulSoup** → HTML ko parse karke required data find karne ke liye
* **Pandas** → Scraped data ko DataFrame me convert karne ke liye
* **NumPy** → Missing values ke liye `np.nan` etc. use karne ke liye

---

## 🌐 Fetching Web Page

Website ka HTML data `requests` se fetch kiya:

```python
webpage = requests.get(url).text
```

Agar website request ko block kare aur **403 Forbidden** aaye, to User-Agent headers ka concept bhi seekha.

---

## 🔍 Parsing HTML

BeautifulSoup se webpage ko parse kiya:

```python
soup = BeautifulSoup(webpage, 'lxml')
```

Iske baad HTML ke elements ko search karke required information extract ki.

---

## 🔎 Finding HTML Elements

### `find()`

Ek matching HTML element find karne ke liye:

```python
soup.find('h1')
```

### `find_all()`

Multiple matching elements find karne ke liye:

```python
soup.find_all('h3')
```

---

## 📝 Extracting Data

Books to Scrape se following information extract ki:

* Book Name
* Price
* Availability
* Rating

Example:

```python
for i in books:
    print(i.find('h3').find('a').get('title'))
```

Price:

```python
i.find('p', class_='price_color').text.strip()
```

Availability:

```python
i.find('p', class_='instock availability').get_text(" ", strip=True)
```

Rating:

```python
i.find('p', class_='star-rating').get('class')[1]
```

---

## 📋 Storing Scraped Data

Alag-alag lists banakar scraped data store kiya:

```python
name = []
price = []
availability = []
rating = []
```

Phir loop ke through data lists me append kiya.

---

## 📊 Creating DataFrame

Scraped lists ko Pandas DataFrame me convert kiya:

```python
df = pd.DataFrame({
    'name': name,
    'price': price,
    'availability': availability,
    'rating': rating
})
```

Ek page se **20 books** ka DataFrame create kiya.

---

## 🔢 DataFrame Inspection

DataFrame ko check karne ke liye:

```python
df.head()
```

```python
df.shape
```

```python
df.info()
```

```python
df.describe()
```

---

## 🔄 Data Cleaning

Scraped price initially text/string form me tha.

Usko numeric form me convert kiya:

```python
df['price'] = df['price'].str.extract(r'([\d.]+)').astype(float)
```

Rating ko numerical values me convert kiya:

```python
rating_map = {
    'One': 1,
    'Two': 2,
    'Three': 3,
    'Four': 4,
    'Five': 5
}

df['rating'] = df['rating'].map(rating_map)
```

---

## 📚 Scraping Multiple Pages

Sirf ek page ke instead multiple pages ko loop ke through scrape kiya.

Books to Scrape ki **50 pages** scrape karke total:

**1000 books × 4 columns**

ka DataFrame banaya.

```python
final = pd.DataFrame()

for page in range(1, 51):
    url = f'https://books.toscrape.com/catalogue/page-{page}.html'

    webpage = requests.get(url).text
    soup = BeautifulSoup(webpage, 'lxml')

    # data extraction

    final = pd.concat([final, temp], ignore_index=True)
```

---

## 🎯 Key Learning

By the end of Day 18, I learned the complete basic workflow:

**Website → Requests → HTML → BeautifulSoup → Extract Data → Lists → Pandas DataFrame → Data Cleaning → Multiple Pages**

### Main Concepts

* Web scraping basics
* `requests`
* BeautifulSoup
* HTML parsing
* `find()`
* `find_all()`
* `.text`
* `.strip()`
* `.get()`
* Extracting attributes
* Lists for storing scraped data
* Creating Pandas DataFrame
* Basic DataFrame inspection
* Converting scraped data into numeric form
* Scraping multiple pages using loops
* Combining multiple DataFrames using `pd.concat()`
