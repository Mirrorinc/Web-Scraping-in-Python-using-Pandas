# Web-Scraping-in-Python-using-Pandas
website: https://www.basketball-reference.com/leagues/NBA_2023_per_game.html

# Web Scraping using Pandas

## Overview
This guide introduces the basics of web scraping using the Pandas library in Python. While Pandas is primarily known for data manipulation, it also supports simple web scraping capabilities. This is particularly useful for extracting data from HTML tables directly into a DataFrame, enabling quick and straightforward data analysis.

## Prerequisites
Before you start, you need to have Python installed on your machine along with the Pandas library. You can install Pandas using pip:

```bash
pip install pandas
```

## How to Scrape Web Tables Using Pandas
Pandas makes it easy to scrape tables from web pages using the `read_html` function. This function reads all the tables found on a web page and returns a list of DataFrames. 

### Step 1: Import Pandas
```python
import pandas as pd
```

### Step 2: Define the URL
Choose the URL from which you want to scrape data. Make sure the page contains tabular data.

```python
url = 'http://example.com/tablepage.html'
```

### Step 3: Use `read_html` to Get Tables
```python
tables = pd.read_html(url)
```

### Step 4: Access the Scraped Data
Since `read_html` returns a list of DataFrames, you can access each table by indexing:
```python
first_table = tables[0]
print(first_table)
```

## Limitations and Considerations
- **Complexity**: Pandas' `read_html` is suitable for straightforward table data but not for more complex or nested HTML structures.
- **Legal and Ethical**: Always ensure you have the right to scrape data from a web page. Check the site's `robots.txt` file and terms of service.
- **Performance**: For large-scale scraping, consider using more robust tools like BeautifulSoup or Scrapy, which offer more control and handle rate limiting and other ethical scraping practices.

## Conclusion
Pandas' `read_html` function provides a fast and efficient method for extracting tables from web pages into DataFrame objects, making it ideal for quick analyses of structured data. For more complex web scraping needs, look into more dedicated libraries like BeautifulSoup or Scrapy.


