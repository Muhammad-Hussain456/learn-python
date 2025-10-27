## 🧭 Control Structures I: Selection Statements (Python Version)

Selection statements in Python help your program **make decisions** based on conditions.

---

## 🔍 Logical Expressions

Logical expressions return either **True** or **False** and are used in decision-making.

**Examples:**
```python
a > b              # True if a is greater than b
x == 10            # True if x equals 10
(x >= 50) and (y >= 50)  # True if both x and y are ≥ 50
```

---

## 🧠 `if` Statement

Executes a block of code **only if** the condition is true.

```python
Syntax:
if condition:
    # code to execute if condition is true
```

**Example:**
```python
score = 75
if score >= 50:
    print("Passed")
```

---

## 🔁 `if-else` Statement

Executes one block if the condition is true, another if false.
Syntax:
```python
if condition:
    # true block
else:
    # false block
```

**Example:**
```python
score = 45
if score >= 50:
    print("Passed")
else:
    print("Failed")
```

---

## 🧩 Nested `if` Statement

An `if` inside another `if`. Used for **multi-level decisions**.

Syntax:
```python
if condition1:
    if condition2:
        # code if both conditions are true
```

**Example:**
```python
score = 85
if score >= 50:
    if score >= 80:
        print("Grade: A")
    else:
        print("Grade: B")
else:
    print("Failed")
```

---

## 🔀 `match` Statement (Python 3.10+)

Used for **multi-way branching** based on a single variable. Similar to `switch` in C++.

```python
match expression:
    case value1:
        # code for value1
    case value2:
        # code for value2
    case _:
        # default case
```

**Example:**
```python
grade = 'B'
match grade:
    case 'A':
        print("Excellent")
    case 'B':
        print("Good")
    case 'C':
        print("Fair")
    case 'F':
        print("Fail")
    case _:
        print("Invalid grade")
```

---

## 🧪 Example Problem: Grade Evaluation

### ✅ Problem:
Evaluate a student's grade and display a message using `if-else` and `match`.

### 💻 Code:
```python
marks = 78

if marks >= 80:
    grade = 'A'
elif marks >= 70:
    grade = 'B'
elif marks >= 60:
    grade = 'C'
else:
    grade = 'F'

match grade:
    case 'A':
        print("Excellent")
    case 'B':
        print("Good")
    case 'C':
        print("Fair")
    case 'F':
        print("Fail")
    case _:
        print("Invalid grade")
```

---
