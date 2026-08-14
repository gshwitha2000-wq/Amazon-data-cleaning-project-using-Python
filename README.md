# Amazon Data Cleaning Project Using Python

## 📌 Project Overview

This project focuses on **cleaning and preprocessing Amazon product data using Python and Pandas**.

Real-world datasets often contain missing values, duplicate records, inconsistent data formats, incorrect data types, and unnecessary columns. This project demonstrates how Python can be used to identify and clean these data-quality issues and prepare the dataset for further analysis.

---

## 🎯 Objectives

* Load the Amazon product dataset using Pandas.
* Explore the structure and contents of the dataset.
* Identify missing values.
* Handle missing and inconsistent data.
* Remove duplicate records.
* Clean unnecessary columns.
* Correct data types and formatting.
* Prepare a clean dataset for analysis.
* Generate useful insights from the cleaned data.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Jupyter Notebook**
* **HTML** – for presenting the project/output
* **CSV** – for storing the dataset

---

## 📂 Project Structure

```text
Amazon-data-cleaning-project-using-Python/
│
├── amazon_product.csv
├── Amazon data cleaning project.html
└── README.md
```

## 🔍 Data Cleaning Process

### 1. Import Required Libraries

```python
import pandas as pd
```

### 2. Load the Dataset

```python
data = pd.read_csv("amazon_product.csv")

print(data.head())
```

### 3. Explore the Dataset

```python
print(data.shape)
print(data.columns)
print(data.info())
print(data.describe())
```

These commands help understand the number of rows, columns, data types, and numerical statistics.

### 4. Check Missing Values

```python
print(data.isnull().sum())
```

Missing values are identified for each column.

### 5. Handle Missing Values

Depending on the column and type of data, missing values can be handled using methods such as:

```python
data = data.ffill()
```

or:

```python
data = data.bfill()
```

For numerical columns, missing values can also be replaced with statistical values such as the mean or median.

### 6. Remove Unnecessary Columns

Columns that are not required for analysis can be removed:

```python
data.drop(columns=['ColumnName'], inplace=True)
```

### 7. Remove Duplicate Records

```python
data.drop_duplicates(inplace=True)
```

This helps ensure that duplicate product records do not affect the analysis.

### 8. Check Data Types

```python
print(data.dtypes)
```

Incorrect data types can be converted using Pandas functions such as:

```python
data['ColumnName'] = pd.to_numeric(
    data['ColumnName'],
    errors='coerce'
)
```

### 9. Verify the Cleaned Dataset

```python
print(data.isnull().sum())
print(data.duplicated().sum())
print(data.info())
```

These checks confirm whether the major data-quality issues have been addressed.

---

## 📊 Data Analysis

After cleaning, the dataset can be used for further analysis, such as:

* Product price analysis
* Product rating analysis
* Review analysis
* Product category analysis
* Discount analysis
* Customer review trends
* Identifying highly rated products
* Comparing product prices

---

## 💡 Key Learning Outcomes

Through this project, I learned how to:

* Work with real-world datasets.
* Import and inspect CSV files using Pandas.
* Identify missing and duplicate data.
* Clean and transform datasets.
* Handle inconsistent data.
* Work with different data types.
* Prepare datasets for exploratory data analysis.
* Use Python for practical data-cleaning tasks.

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/gshwitha2000-wq/Amazon-data-cleaning-project-using-Python.git
```

### Step 2: Navigate to the Project

```bash
cd Amazon-data-cleaning-project-using-Python
```

### Step 3: Install Pandas

```bash
pip install pandas
```

### Step 4: Run the Python/Jupyter Analysis

Open the HTML file or run the corresponding analysis in Jupyter Notebook.

---

## 👩‍💻 Author

**Ashwitha Gogikar**

GitHub:
https://github.com/gshwitha2000-wq

LinkedIn:
https://www.linkedin.com/in/ashwitha-gogikar-35839a1b5/

---

## ⭐ Project Summary

**Amazon Data Cleaning Project using Python** demonstrates the practical use of **Pandas for data cleaning and preprocessing**. The project takes a raw Amazon product dataset and applies common data-cleaning techniques to make the data more reliable, consistent, and ready for further analysis.
