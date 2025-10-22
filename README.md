# 📱 Mobile & Laptop Sales Data Analysis (Python | Pandas | Seaborn)

## 🧾 Overview
This project explores and analyzes **mobile and laptop sales data** using Python.  
It focuses on **data cleaning, preprocessing, correlation analysis, and visualization** to identify patterns such as sales trends, pricing relationships, and outlier behavior.

The dataset used in this project (`mobile_sales_data.csv`) contains detailed information about customer purchases, product specifications, and sales metrics across different regions.

---

## 🧰 Technologies Used
- **Python 3.10+**
- **Pandas** → Data loading, cleaning, and transformation  
- **NumPy** → Numerical operations  
- **Seaborn** → Statistical data visualization  
- **Matplotlib** → Charting and plots  

---

## 📂 Dataset Information
**File:** `mobile_sales_data.csv`  
**Rows:** 50,000  
**Columns:** 16  

| Column Name | Description |
|--------------|-------------|
| `Product` | Type of product (e.g., Mobile Phone, Laptop) |
| `Brand` | Brand name (e.g., Samsung, Sony, Apple) |
| `Product Code` | Unique product identifier |
| `Product Specification` | Text description of the product |
| `Price` | Selling price of the item |
| `Inward Date` | Date product was received |
| `Dispatch Date` | Date product was sold/dispatched |
| `Quantity Sold` | Number of units sold |
| `Customer Name` | Name of the customer |
| `Customer Location` | City/town of the customer |
| `Region` | Regional zone (e.g., North, South, East, Central) |
| `Core Specification` | CPU/Chipset details |
| `Processor Specification` | Processor model (e.g., i7, Ryzen 5) |
| `RAM` | Random Access Memory size |
| `ROM` | Storage capacity |
| `SSD` | SSD size (if available) |

---

## 🧹 Data Cleaning Steps
The dataset underwent the following cleaning and preprocessing steps:

1. **Loaded** CSV file using `pandas.read_csv()`.
2. **Inspected** data with `.head()`, `.info()`, `.describe()`, and `.shape`.
3. **Handled missing values:**
   - Filled numeric columns with column mean (`df.fillna(df.mean())`).
   - Filled categorical columns with the most frequent value (mode).
4. **Dropped duplicates** using `df.drop_duplicates()`.
5. **Standardized text columns** (converted all string values to lowercase).
6. **Converted date columns** (`Inward Date`, `Dispatch Date`) to datetime format (optional step).
7. **Explored correlations** between numerical columns like `Price` and `Quantity Sold`.
8. **Visualized** key relationships using histograms, boxplots, and heatmaps.

---

## 📊 Exploratory Data Analysis (EDA)

### 🔹 1. Histogram for Numeric Columns
Displays data distribution for `Price` and `Quantity Sold`.
```python
df.hist(figsize=(10, 6))
plt.show()
