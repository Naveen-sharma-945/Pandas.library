

---

### 🧠 **What is Pandas?**

**Definition:**
Pandas is a **Python library** used for **data analysis and manipulation**.
It provides two main data structures:

* **Series** → 1-dimensional labeled array (like a column in Excel).
* **DataFrame** → 2-dimensional table (like an Excel sheet or SQL table).

Pandas is built on top of **NumPy** and integrates well with **Matplotlib**, **Seaborn**, and **Scikit-learn** for data science tasks.

---

### ⚙️ **Why use Pandas?**

✅ Handle large datasets easily
✅ Clean, transform, and analyze data
✅ Import/export data (CSV, Excel, SQL, JSON, etc.)
✅ Handle missing values
✅ Perform grouping, merging, filtering, sorting
✅ Visualize data quickly

---

### 💻 **Installation (pip)**

```bash
pip install pandas
```

(Optional: for better compatibility)

```bash
pip install numpy matplotlib openpyxl xlrd pyarrow
```

---

### 🧩 **Importing Pandas**

```python
import pandas as pd
```

*(We usually use `pd` as a short name for pandas.)*

---

### 📗 **Basic Data Structures in Pandas**

#### 1. 🧮 **Series**

A **Series** is a one-dimensional labeled array.

```python
import pandas as pd

# Create a simple Series
s = pd.Series([10, 20, 30, 40])

print(s)
```

**Output:**

```
0    10
1    20
2    30
3    40
dtype: int64
```

➡ The left side (0,1,2,3) is the **index**.
➡ The right side is the **data**.

---

#### 2. 📊 **DataFrame**

A **DataFrame** is a 2D table made up of multiple Series.

```python
data = {
    'Name': ['Amit', 'Riya', 'Karan'],
    'Age': [21, 23, 22],
    'Marks': [85, 90, 88]
}

df = pd.DataFrame(data)

print(df)
```

**Output:**

```
    Name  Age  Marks
0   Amit   21     85
1   Riya   23     90
2  Karan   22     88
```

---


### 🎯 **Selecting Data**

```python
# Select one column
df['Name']

# Select multiple columns
df[['Name', 'Marks']]

# Select rows using index
df.loc[0]          # label-based
df.iloc[1]         # position-based
```

---

### 🧹 **Data Cleaning Basics**

```python
df.isnull()          # Check for missing values
df.dropna()          # Remove missing rows
df.fillna(0)         # Replace missing values with 0
df.duplicated()      # Check for duplicates
df.drop_duplicates() # Remove duplicates
```

---

### 🧮 **Basic Operations**

```python
# Add a new column
df['Grade'] = ['B', 'A', 'A']

# Sort by a column
df.sort_values(by='Marks', ascending=False)

# Filter rows
df[df['Marks'] > 85]

# Compute mean and sum
df['Marks'].mean()
df['Marks'].sum()
```

---

### 🔗 **Combining Data**

```python
# Concatenate DataFrames
pd.concat([df1, df2])

# Merge (like SQL JOIN)
pd.merge(df1, df2, on='ID')
```

---

### 📥 **Input/Output Operations**

```python
# Read CSV
df = pd.read_csv('data.csv')

# Write CSV
df.to_csv('output.csv', index=False)

# Read Excel
df = pd.read_excel('data.xlsx')

# Write Excel
df.to_excel('output.xlsx', index=False)
```

---

### 📈 **Basic Visualization**

```python
import matplotlib.pyplot as plt

df.plot(kind='bar', x='Name', y='Marks', color='teal')
plt.title('Marks of Students')
plt.xlabel('Name')
plt.ylabel('Marks')
plt.show()
```

---

### 💡 **Quick Reference (Cheat Sheet)**

| Operation        | Command                    |
| ---------------- | -------------------------- |
| Create Series    | `pd.Series([10,20,30])`    |
| Create DataFrame | `pd.DataFrame(dict)`       |
| Head/Tail        | `df.head(), df.tail()`     |
| Column selection | `df['col']`                |
| Row selection    | `df.loc[], df.iloc[]`      |
| Filter           | `df[df['col']>value]`      |
| Sort             | `df.sort_values('col')`    |
| Describe         | `df.describe()`            |
| Group            | `df.groupby('col').mean()` |
| Export CSV       | `df.to_csv('file.csv')`    |

---

Would you like me to continue with **“Intermediate Pandas Concepts”** next (like GroupBy, Aggregations, Merging, Pivot Tables, and Time Series)?
I’ll include full explanations + copy-ready examples for each.

