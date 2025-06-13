# 🐼 Pandas Mastery Guide – From Beginner to Pro 🔥

> 💡 The ultimate Pandas learning repository – covering everything from data loading to advanced transformations, real-world examples, group-by operations, and project-ready use-cases.

---

## 📌 Table of Contents

- [🌟 Why Pandas?](#-why-pandas)
- [🧠 Core Concepts](#-core-concepts)
  - [Loading & Creating Data](#loading--creating-data)
  - [Indexing & Selection](#indexing--selection)
  - [Filtering & Conditional Logic](#filtering--conditional-logic)
- [🧮 Aggregation & Grouping](#-aggregation--grouping)
- [🧹 Data Cleaning](#-data-cleaning)
- [🔗 Joining & Merging](#-joining--merging)
- [🗓️ Time Series](#️-time-series)
- [📦 Advanced Pandas](#-advanced-pandas)
- [🛠️ Real-Life Use-Cases](#️-real-life-use-cases)
- [📘 Practice Problems](#-practice-problems)
- [📚 Resources](#-resources)
- [🧪 Project Ideas](#-project-ideas)
- [✅ Quiz & Checklist](#-quiz--checklist)

---

## 🌟 Why Pandas?

Pandas is the most powerful data analysis library in Python. Whether you're cleaning, transforming, visualizing, or feeding data into models, Pandas is your essential tool for **data wrangling** and **exploration**.

---

## 🧠 Core Concepts

### 📌 Loading & Creating Data
```python
import pandas as pd

df = pd.read_csv('data.csv')          # Load CSV
pd.read_excel('data.xlsx')            # Load Excel
pd.DataFrame({'A': [1, 2], 'B': [3, 4]})  # Create DataFrame
```

### 🔍 Indexing & Selection
```python
df['Column'], df[['C1', 'C2']]        # Column selection
df.iloc[0]                            # Row by position
df.loc[0]                             # Row by label
df.at[0, 'A'], df.iat[0, 1]           # Fast access
```

### 🔎 Filtering & Conditional Logic
```python
df[df['Age'] > 25]                    # Conditional filter
df[(df['Age'] > 25) & (df['Gender'] == 'M')]
df.query('Age > 25 and Gender == "M"')  # Query strings
```

---

## 🧮 Aggregation & Grouping
```python
df.groupby('City')['Sales'].mean()
df.groupby(['City', 'Gender']).agg({'Sales': 'sum'})
df.pivot_table(index='City', columns='Gender', values='Sales', aggfunc='mean')
```

---

## 🧹 Data Cleaning

```python
df.isnull().sum()                     # Missing values
df.dropna(), df.fillna(0)             # Handle missing
df.duplicated().sum(), df.drop_duplicates()
df['Amount'] = df['Amount'].astype('float')
df.columns = df.columns.str.lower().str.replace(' ', '_')
```

---

## 🔗 Joining & Merging
```python
pd.concat([df1, df2], axis=0)         # Stack rows
pd.merge(df1, df2, on='CustomerID')   # Join on key
pd.merge(df1, df2, how='outer')       # Full outer join
```

---

## 🗓️ Time Series

```python
df['Date'] = pd.to_datetime(df['Date'])
df.set_index('Date', inplace=True)
df['2023-01'].resample('M').sum()
```

---

## 📦 Advanced Pandas

```python
df['Category'] = df['Product'].apply(lambda x: x.split()[0])
df['Profit Margin'] = df['Profit'] / df['Sales']
df = df.sort_values(by='Amount', ascending=False)
df = df.assign(Rank=df['Sales'].rank(ascending=False))
```

---

## 🛠️ Real-Life Use-Cases

- Retail sales analytics
- Healthcare patient data preprocessing
- Social media engagement breakdown
- Time-series forecasting prep
- EDA (Exploratory Data Analysis) pipelines

---

## 📘 Practice Problems

✅ Load CSV and filter rows based on column values  
✅ Group sales by city and gender  
✅ Clean null values and convert columns to proper types  
✅ Extract month from datetime and calculate monthly totals  
✅ Merge two datasets and identify common entries

---



## 📚 Resources

- [Pandas Official Docs](https://pandas.pydata.org/docs/)
- [Kaggle Pandas Course](https://www.kaggle.com/learn/pandas)
- [Data School Pandas YouTube Series](https://www.youtube.com/playlist?list=PL5-da3qGB5ICCsgW1MxlZ0Hq8LL5U3u9y)
- [Pandas 100 Exercises GitHub](https://github.com/guipsamora/pandas_exercises)

---

## 🧪 Project Ideas

- 📊 Retail Sales Dashboard with GroupBy & Pivot
- 🧼 Hospital Dataset Cleaner Tool
- 🗓️ Time Series Sales Analysis App
- 👥 Customer Segmentation Engine
- 📄 Resume Parser with Text Cleaning using Pandas

---

## ✅ Quiz & Checklist

### ✅ Quick Quiz
1. Difference between `.loc[]` and `.iloc[]`?
2. What does `groupby().agg()` do?
3. How to drop missing values?
4. What is the use of `.apply()` function?
5. How do you convert strings to datetime in Pandas?

 

---

### 🚀 Final Words

> Master Pandas and you unlock the full power of **data wrangling, cleaning, exploration, and transformation**. This is your strongest weapon in the data science toolkit! 💥

🌟 Star this repo and check out my other guides on NumPy, Matplotlib, Seaborn & Scikit-learn for full-stack data science mastery!

---
