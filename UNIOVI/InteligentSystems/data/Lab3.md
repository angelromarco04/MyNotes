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

data_train, data_test =
sk.model_selection.train_test_split(data, test_size=0.2, random_state=2533)
```
---
## Scikit-Learn
```python
from sklearn import metrics
from sklearn.preprocessing import StandardScaler

# Select the model to use to predict (See below)
model = DummyClassifier()

# Obtain the data for training
X = data_train["MyCol_1", "MyCol_2", "MyCol_3"]
Y = data_train["Solution"]

# Obtain data for testing
X_test = data_test["MyCol_1", "MyCol_2", "MyCol_3"]
Y_test = data_test["Solution"]

# Sometimes it is important to normalize
standardizer = StandardScaler()
X_std = standardizer.fit_transform(X)
X_test_std = standardizer.transform(X_test)

# Train the model
model.fit(X, Y)

# Make predictions
Y_pred = model.predict(X_test)

# Evaluate the prediction
metrics.confusion_matrix(Y_test, Y_pred) # True/False Positives/Negatives
metrics.precision_score(Y_test, Y_pred) # Used when false positives are costly
metrics.accuracy_score(Y_test, Y_pred) # Percentaje of hits (for balanced data)
metrics.f1_score(Y_test, Y_pred) # For inbalance data (precision and recall matter)

```