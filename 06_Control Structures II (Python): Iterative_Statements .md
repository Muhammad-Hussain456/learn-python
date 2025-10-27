# 🔁 Control Structures II (Python): Iterative_Statements / loops

Iterative Statements / loops allow your program to **repeat actions** efficiently based on conditions or sequences.

---

## 🔄 `for` Loop

### ✅ Syntax
```python
for variable in iterable:
    # code block to execute
```

### 📘 Semantic  
Iterates over each item in a sequence (like a list, string, or range).

### 💡 Example
```python
for i in range(5):
    print("Iteration", i)
```
This prints numbers from 0 to 4.

---

## 🔁 `while` Loop

### ✅ Syntax
```python
while condition:
    # code block to execute
```

### 📘 Semantic  
Repeats the block **as long as** the condition is `True`.

### 💡 Example
```python
count = 0
while count < 5:
    print("Count:", count)
    count += 1
```

---

## 🔁 `do-while` Equivalent in Python

Python does **not** have a built-in `do-while` loop, but you can simulate it using `while True` and a `break`.

### ✅ Syntax
```python
while True:
    # code block
    if not condition:
        break
```

### 📘 Semantic  
Executes the block **at least once**, then repeats based on a condition.

### 💡 Example
```python
count = 0
while True:
    print("Count:", count)
    count += 1
    if count >= 5:
        break
```

---

## 🔁 Nested Loops

### ✅ Syntax
```python
for outer in range(n):
    for inner in range(m):
        # code block
```

### 📘 Semantic  
A loop inside another loop. Useful for grids, matrices, or combinations.

### 💡 Example
```python
for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
```

---
