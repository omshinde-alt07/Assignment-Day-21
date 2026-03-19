# Regression vs Classification and Bias-Variance Tradeoff

## 1. Prompt Given to AI

"Explain regression vs classification and bias-variance tradeoff with Python examples and visualizations."

---

## 2. AI Output (with Examples)

### Regression vs Classification

Regression is used when the output variable is continuous. For example, predicting house prices or temperature.

Classification is used when the output variable is categorical. For example, spam detection or pass/fail prediction.

#### Regression Example:

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

X = np.random.rand(100, 1) * 10
y = 3 * X.squeeze() + 5

model = LinearRegression()
model.fit(X, y)

y_pred = model.predict(X)

plt.scatter(X, y)
plt.plot(X, y_pred, color='red')
plt.title("Regression")
plt.show()
```

#### Classification Example:

```python
from sklearn.linear_model import LogisticRegression

X = np.random.rand(100, 1) * 10
y = (X.squeeze() > 5).astype(int)

model = LogisticRegression()
model.fit(X, y)

plt.scatter(X, y)
plt.title("Classification")
plt.show()
```

---

### Bias-Variance Tradeoff

Bias is error due to a simple model (underfitting), while variance is error due to a complex model (overfitting).

#### Example:

```python
from sklearn.preprocessing import PolynomialFeatures
from sklearn.metrics import mean_squared_error

X = np.linspace(0, 10, 100).reshape(-1, 1)
y = np.sin(X).ravel()

degrees = [1, 2, 5]

for d in degrees:
    poly = PolynomialFeatures(degree=d)
    X_poly = poly.fit_transform(X)
    model = LinearRegression()
    model.fit(X_poly, y)
    y_pred = model.predict(X_poly)
    plt.plot(X, y_pred, label=f"Degree {d}")

plt.scatter(X, y)
plt.legend()
plt.title("Bias vs Variance")
plt.show()
```

---

## 3. Evaluation

### Are the explanations correct?

Yes, the explanations are correct. Regression and classification are clearly differentiated based on the type of target variable. The bias-variance concept is also explained correctly with underfitting and overfitting.

---

### Do visualizations correctly show underfitting and overfitting?

Yes, the visualizations correctly demonstrate underfitting and overfitting. The lower degree polynomial (degree 1) underfits the data, while the higher degree polynomial (degree 5) overfits. The medium degree (degree 2) provides a better fit.

---

## Conclusion

This assignment helped me understand the difference between regression and classification and how bias-variance tradeoff affects model performance. Visualiza
