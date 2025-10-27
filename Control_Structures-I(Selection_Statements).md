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

## 🔍 Logical Expressions – Syntax, Semantics, and Examples

| 🔣 Syntax                          | 📘 Semantic Meaning                                      | 💡 Example                            |
|-----------------------------------|----------------------------------------------------------|---------------------------------------|
| `operand1 == operand2`            | Checks if both operands are equal                        | `5 == 5` → `True`                     |
| `operand1 != operand2`            | Checks if operands are not equal                         | `5 != 3` → `True`                     |
| `operand1 > operand2`             | Checks if left operand is greater than right             | `7 > 4` → `True`                      |
| `operand1 < operand2`             | Checks if left operand is less than right                | `3 < 9` → `True`                      |
| `operand1 >= operand2`            | Checks if left operand is greater than or equal to right | `6 >= 6` → `True`                     |
| `operand1 <= operand2`            | Checks if left operand is less than or equal to right    | `2 <= 5` → `True`                     |
| `(condition1) and (condition2)`   | True if **both** conditions are true                     | `(5 > 3) and (2 < 4)` → `True`        |
| `(condition1) or (condition2)`    | True if **at least one** condition is true               | `(5 > 3) or (2 > 4)` → `True`         |
| `not(condition)`                  | True if the condition is **false**                       | `not(5 == 3)` → `True`                |

---

## 🧠 `if` Statement

Semantic:
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
Semantic:
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
Semantic:
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

Semantic:
Used for **multi-way branching** based on a single variable. Similar to `switch` in C++.

Syntax:
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
