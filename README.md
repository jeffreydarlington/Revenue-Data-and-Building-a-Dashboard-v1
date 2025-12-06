# 📈 Extracting and Visualizing Stock Data

This project focuses on extracting historical stock prices and revenue data for **Tesla (TSLA)** and **GameStop (GME)** using **yfinance**, **web scraping**, **pandas**, and **Matplotlib**.
It demonstrates end-to-end data extraction, cleaning, transformation, and visualization — essential skills in real-world data analysis.

---

## 🔍 Project Overview

In this project, you will:

* Use **yfinance** to pull historical stock price data
* Use **web scraping** to extract quarterly revenue data
* Clean, filter, and structure financial datasets
* Visualize stock price trends and revenue performance
* Build reusable functions for data visualization
* Produce insights by combining multiple datasets

This mirrors real data-pipeline workflows used in financial analytics, business intelligence, and data science.

---

## 📂 Table of Contents

* Define a Graphing Function
* Extract Tesla Stock Data (yfinance)
* Webscrape Tesla Revenue Data (BeautifulSoup)
* Extract GameStop Stock Data (yfinance)
* Webscrape GameStop Revenue Data (BeautifulSoup)
* Plot Tesla Stock & Revenue Graph
* Plot GameStop Stock & Revenue Graph

**Estimated Time:** 30 minutes

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Matplotlib**
* **BeautifulSoup (bs4)**
* **Requests**
* **yfinance**
* **Jupyter Notebook**

---

## 📦 Installation

If running locally, install dependencies:

```bash
pip install yfinance
pip install bs4
pip install matplotlib
pip install nbformat
```

You will also need:

```python
import yfinance as yf
import pandas as pd
import requests
from bs4 import BeautifulSoup
import matplotlib.pyplot as plt
import warnings

warnings.filterwarnings("ignore", category=FutureWarning)
```

---

## 📊 Graphing Function

The project includes a reusable function, `make_graph`, which takes:

* a stock price DataFrame (`Date`, `Close`)
* a revenue DataFrame (`Date`, `Revenue`)
* a stock name

It produces two stacked Matplotlib graphs:

1. Historical Stock Price
2. Historical Revenue

This function is used later to plot **Tesla** and **GameStop** performance.

---

## 🚗 Question 1: Extract Tesla Stock Data (yfinance)

* Create a ticker object using `yf.Ticker("TSLA")`
* Pull *maximum* historical data using `.history(period="max")`
* Reset the index
* Display the first rows of the DataFrame

---

## 🚗 Question 2: Webscrape Tesla Revenue Data

* Download the revenue webpage with `requests`
* Parse HTML with `BeautifulSoup`
* Locate the Tesla quarterly revenue table
* Extract rows into a DataFrame with `Date` and `Revenue`
* Clean formatting (remove commas & $ signs)
* Drop empty values

---

## 🎮 Question 3: Extract GameStop Stock Data (yfinance)

* Create ticker object: `yf.Ticker("GME")`
* Pull full historical data
* Reset index
* Display first rows

---

## 🎮 Question 4: Webscrape GameStop Revenue Data

* Download GameStop revenue webpage
* Parse table similar to Tesla
* Extract quarterly revenue table
* Clean Revenue column
* Display last rows

---

## 📈 Question 5: Plot Tesla Graph

```python
make_graph(tesla_data, tesla_revenue, "Tesla")
```

Generates Tesla’s **stock price** and **revenue** trends up to June 2021.

---

## 📈 Question 6: Plot GameStop Graph

```python
make_graph(gme_data, gme_revenue, "GameStop")
```

Generates GameStop’s **stock price** and **revenue** trends up to June 2021.

---

## 👨‍🏫 About the Authors

* **Joseph Santarcangelo** – PhD in Electrical Engineering, IBM Machine Learning Research
* **Azim Hirjani**

---

## 📝 Change Log

| Date       | Version | Changed By    | Description              |
| ---------- | ------- | ------------- | ------------------------ |
| 2022-02-28 | 1.2     | Lakshmi Holla | Updated GameStop URL     |
| 2020-11-10 | 1.1     | Malika Singla | Removed optional section |
| 2020-08-27 | 1.0     | Malika Singla | Initial release          |

---

## 📜 License

© 2020 IBM Corporation — All Rights Reserved.

---
