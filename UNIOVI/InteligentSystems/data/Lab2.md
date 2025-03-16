# Data preprocessing & Visualization
---
[Go Back](../README.md)

---
## Objectives
- Understand the data
- Remove or fill empty rows or columns
- Eliminate inconsistent values
---
## Obtaining the data
```python
import pandas as pd

data_source = "..." # Can be an URL or a local path.

# Read from csv file 
data = pd.read_csv(data_source)

# Read from pickle file (Serialize oython objects - More storage efficient)
data = pd.read_pickle(data_source)

# Read from JSON file
data = pd.read_json(data_source)

# Read from a sheet of an Excel file
data = pd.read_excel('data.xlsx', sheet_name='Sheet1')
```
---
## Exploring the data
### Counting columns & rows
```python
# Count rows
len(data)

# Get list of column names
data.columns

# Count columns
len(data.columns)

# Get a tuple (number rows , number columns)
data.shape
```
### Accessing the data
```python
# Accesss the first N rows
data.head(N)

# Accesss the last N rows
data.tail(N)

# Access a column
data['MyCol']

# Access multiple columns
data[['Driver', 'Team']]

# Get the row number N as a DataFrame
data.loc[N]

# Access a position
data.loc[row, col]

# Get an array representation
data.values
```
### Statistics
```python
# For each column obtaine number non-null and type
data.info()

# Get statistics all columns or an specific columns
data.describe()
data['MyCol'].describe()

# Get unique values for a column
data['MyCol'].unique()

# Get if there are empty values
data.isnull().any()
data['MyCol'].isnull().any()

# Get the number of empty values
data.isnull().sum()
data['MyCol'].isnull().sum()

# Other statistics
data['MyCol'].mean()   # Mean (average)
data['MyCol'].median() # Median
data['MyCol'].mode()   # Mode (most frequent value)
data['MyCol'].min()
data['MyCol'].max()
data['MyCol'].std()  # Standard deviation
data['MyCol'].var()  # Variance
```
---
## Changing types
```python
# Check data types of each column
data.dtypes

# Change column type to integer
data['MyCol'] = data['MyCol'].astype(int)

# Change column type to float
data['MyCol'] = data['MyCol'].astype(float)

# Change column type to string
data['MyCol'] = data['MyCol'].astype(str)

```