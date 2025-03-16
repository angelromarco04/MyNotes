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