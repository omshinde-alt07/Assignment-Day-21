# NumPy Broadcasting and Vectorisation

## 1. Prompt Given to AI

"Explain NumPy broadcasting and vectorisation with practical Python examples."

---

## 2. AI Output (with Examples)

### NumPy Broadcasting

NumPy broadcasting allows operations between arrays of different shapes by automatically expanding the smaller array.

#### Example:

```python
import numpy as np

A = np.array([[1, 2, 3],
              [4, 5, 6]])

B = np.array([10, 20, 30])

print(A + B)
```

#### Output:

```
[[11 22 33]
 [14 25 36]]
```

Explanation: The 1D array is stretched to match the rows of the 2D array.

---

### Vectorisation

Vectorisation means performing operations on entire arrays without using loops.

#### Example:

```python
arr = np.array([1, 2, 3, 4])
result = arr * 2
print(result)
```

#### Output:

```
[2 4 6 8]
```

Loop version (slower):

```python
result = []
for i in range(len(arr)):
    result.append(arr[i] * 2)
```

---

## 3. Evaluation

### Are the examples correct?

Yes, the examples are correct. Broadcasting is properly demonstrated by adding a 1D array to a 2D array. The vectorisation example correctly shows element-wise multiplication.

---

### Is the code efficient and runnable?

Yes, the code is efficient and runnable. NumPy operations are used instead of loops, which improves performance. The examples are simple and can be executed without any errors.

---

## Conclusion

This task helped me understand how broadcasting and vectorisation work in NumPy. Broadcasting simplifies operations on different shaped arrays, while vectorisation improves speed by avoiding loops.
