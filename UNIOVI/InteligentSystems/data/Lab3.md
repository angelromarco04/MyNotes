# Data Classification
---
[Go Back](../README.md)

---
## Baseline
### Random
```python
import random
random.seed(2533)

random_values = [random.choice([0, 1]) for _ in range(len(data))]
```
### Zero-R
We always predict the most frequent value for a column.
```python
mode = data_aston['MyCol'].mode().value

zero_r_values = [mode for _ in range(len(data))]
```
---
## Dividing subsets
```python
import sklearn as sk # type: ignore

# Divide the dataset int 80% for training and 20% for testing

data_train, data_test = sk.model_selection.train_test_split(data_aston, test_size=0.2, random_state=2533)
```