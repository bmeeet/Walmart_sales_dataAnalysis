
# 🛒 Walmart Sales Data Analysis (Python + PostgreSQL)

This project explores Walmart sales data using **Python** and **PostgreSQL** to gain insights into sales trends, customer behavior, and business performance. The data is cleaned, processed, and analyzed through SQL queries and Python scripts.

---

## 🚀 Project Goals

- Load and clean Walmart sales data using Python.
- Store the cleaned data in a PostgreSQL database.
- Perform business-critical SQL analysis.
- Share insights through documented queries and notebooks.

---

## 🧰 Technologies Used

- **Languages**: Python 3.8+
- **Database**: PostgreSQL
- **Libraries**: pandas, numpy, sqlalchemy, psycopg2
- **Tools**: Jupyter Notebook, Kaggle API, VS Code

---


## 🪜 Step-by-Step Guide

### 1. Set Up Kaggle API

- Go to [Kaggle](https://www.kaggle.com/account), download your `kaggle.json` API token.
- Place it in:
  - Windows: `C:\Users\<username>\.kaggle\kaggle.json`
  - Mac/Linux: `~/.kaggle/kaggle.json`

### 2. Download the Dataset

```bash
kaggle datasets download -d <dataset-name>
unzip *.zip -d data/
```

### 3. Explore & Clean the Data

- Remove duplicates and missing values
- Convert data types (e.g., dates, prices)
- Add computed columns (e.g., `Total Amount`)

### 4. Load Data into PostgreSQL

Update your database credentials in `main.py` and run the script to insert cleaned data into a PostgreSQL table.

### 5. Run SQL Analysis

Write SQL queries to answer questions such as:

- Revenue by branch or category
- Best-selling items
- Customer payment preferences
- Profitability trends

---

## 📊 Example SQL Insight

```sql
-- Top 3 Categories by Revenue
SELECT category, SUM(total_amount) AS revenue
FROM walmart_sales
GROUP BY category
ORDER BY revenue DESC
LIMIT 3;
```

---

## 📌 Key Insights (Sample)

- **Top Revenue Branch**: Branch A
- **Preferred Payment Method**: Ewallet
- **Most Profitable Category**: Electronics
- **Sales Peaks**: Weekends and 1 PM – 3 PM

---

## 🧠 Future Enhancements

- Connect to Power BI/Tableau for live dashboards
- Automate data ingestion pipeline
- Add customer segmentation and forecasting

---

## 📄 License

This project is intended for educational and portfolio use. Contributions welcome!
