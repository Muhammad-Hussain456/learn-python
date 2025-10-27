## 🧭 Control Structures I (Python)

---

## 🔍 Expressions in Python

An **expression** is any valid combination of operands and operators that evaluates to a value.

### ✅ Types of Expressions

| 🧩 Type            | ✅ Syntax                          | 📘 Semantic Meaning                                      | 💡 Example                      |
|--------------------|------------------------------------|----------------------------------------------------------|---------------------------------|
| Arithmetic         | `operand1 + operand2`              | Performs math operations                                 | `a + b` → adds `a` and `b`      |
| Relational         | `operand1 > operand2`              | Compares values, returns `True` or `False`               | `score > 50` → `True` if score is above 50 |
| Logical            | `condition1 and condition2`        | Combines Boolean results                                 | `(x > 5) and (y < 10)` → `True` if both are true |
| Assignment         | `variable = value`                 | Assigns a value to a variable                            | `x = 10` → assigns 10 to `x`    |
| Unary              | `not condition`                    | Operates on a single operand                             | `not flag` → negates `flag`     |
| Compound           | `variable += value`                | Combines arithmetic and assignment                       | `x += 5` → adds 5 to `x`         |

---

## 🧾 Statements in Python

A **statement** is a complete instruction that performs an action. It may contain expressions.

### ✅ Types of Statements

| 🧩 Type                  | ✅ Syntax Example                  | 📘 Semantic Meaning                                      | 💡 Example                      |
|--------------------------|------------------------------------|----------------------------------------------------------|---------------------------------|
| Expression Statement     | `expression`                       | Evaluates an expression                                  | `x = 5`                         |
| Declaration Statement    | `variable = value`                 | Declares and initializes a variable                      | `score = 90`                    |
| Compound Statement       | `if x > 0:\n    print(x)`          | Groups multiple statements via indentation               | `if x > 0:\n    print(x)`       |
| Selection Statement      | `if`, `if-else`, `match`           | Chooses between paths based on conditions                | `if x > 0: print(x)`            |
| Iteration Statement      | `for`, `while`                     | Repeats actions based on conditions                      | `while x < 10:\n    x += 1`     |
| Jump Statement           | `break`, `continue`, `return`      | Alters control flow directly                             | `return "Done"`                |

---

### Selection Statement  
Selection statements in Python allow your program to **make decisions** based on conditions.

---

### 🧠 `if` Statement

#### ✅ Syntax
```python
if condition:
    # code to execute if condition is true
```

#### 📘 Semantic  
Executes the block only if the condition evaluates to `True`.

#### 💡 Example
```python
score = 75
if score >= 50:
    print("Passed")
```

---

### 🔁 `if-else` Statement

#### ✅ Syntax
```python
if condition:
    # true block
else:
    # false block
```

#### 📘 Semantic  
Executes one block if the condition is true, another if false.

#### 💡 Example
```python
score = 45
if score >= 50:
    print("Passed")
else:
    print("Failed")
```

---

### 🧩 Nested `if` Statement

#### ✅ Syntax
```python
if condition1:
    if condition2:
        # code if both conditions are true
```

#### 📘 Semantic  
Allows multi-level decision-making by nesting conditions.

#### 💡 Example
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

### 🔀 `match` Statement (Python 3.10+)

#### ✅ Syntax
```python
match expression:
    case value1:
        # code for value1
    case value2:
        # code for value2
    case _:
        # default case
```

#### 📘 Semantic  
Selects one of many possible blocks to execute based on a single expression.

#### 💡 Example
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

Would you like this exported into your Markdown or Word template next? I can also prepare a bilingual version with Urdu translations for each semantic label and comment.
