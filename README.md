# multiple-linear-regression-small
# Boston Housing Price Prediction

This project demonstrates a simple implementation of linear regression using scikit-learn to predict housing prices in Boston based on various features such as crime rate, number of rooms, distance to employment centers, and more.

> **Note**: The `load_boston()` dataset is deprecated in scikit-learn 1.2+. This project uses it for educational purposes only. For future work, consider using the `fetch_california_housing()` dataset.

---

## 📊 Dataset

- **Source**: `sklearn.datasets.load_boston()`
- **Target variable**: Median value of owner-occupied homes in $1000s.
- **Number of samples**: 506
- **Number of features**: 13 (e.g., crime rate, number of rooms, property tax rate)

---

## 🧠 Model

- **Algorithm**: Linear Regression
- **Library**: `sklearn.linear_model.LinearRegression`

### Model Training
```python
from sklearn.linear_model import LinearRegression
from sklearn.datasets import load_boston

# Load data
boston_data = load_boston()
x = boston_data['data']
y = boston_data['target']

# Train model
model = LinearRegression()
model.fit(x, y)
