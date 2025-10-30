# 📦 Arrays in Python

In Python, arrays can be represented using:
- **Lists** (built-in, flexible, dynamic)
- **NumPy arrays** (efficient, typed, used in scientific computing)

---

## 🔹 One-Dimensional Arrays

### ✅ Syntax (List-based)
```python
array = [value1, value2, value3]
```

### 📘 Semantic Meaning  
A linear collection of elements accessed by index.

### 💡 Example
```python
fruits = ["apple", "banana", "cherry"]
print(fruits[1])  # Output: banana
```

---

## 🔹 Multi-Dimensional Arrays

### ✅ Syntax (List of lists)
```python
array = [[row1_values], [row2_values], ...]
```

### 📘 Semantic Meaning  
A grid-like structure where each sublist represents a row.

### 💡 Example
```python
matrix = [[1, 2], [3, 4]]
print(matrix[1][0])  # Output: 3
```

### ✅ Syntax (NumPy)
```python
import numpy as np
array = np.array([[1, 2], [3, 4]])
```

---

## 🔧 Array Operations

### ✅ Accessing Elements
```python
array[index]
```

### ✅ Modifying Elements
```python
array[index] = new_value
```

### ✅ Iterating Over Elements
```python
for item in array:
    print(item)
```

### ✅ Length of Array
```python
len(array)
```

### ✅ Slicing
```python
array[start:end]
```

### 💡 Example
```python
numbers = [10, 20, 30, 40, 50]
print(numbers[1:4])  # Output: [20, 30, 40]
```

---

## 🧠 Passing Arrays to Functions

### ✅ Syntax
```python
def process_array(arr):
    for item in arr:
        print(item)

process_array([1, 2, 3])
```

### 📘 Semantic Meaning  
Arrays (lists or NumPy arrays) can be passed as arguments to functions and manipulated inside.

---

## 🔬 NumPy-Specific Operations (Optional for Advanced Learners)

```python
import numpy as np

arr = np.array([[1, 2], [3, 4]])

print(arr.shape)       # (2, 2)
print(arr[0, 1])       # 2
print(arr.T)           # Transpose
print(arr.flatten())   # Convert to 1D
```

---
