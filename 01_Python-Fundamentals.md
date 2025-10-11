
**For Basics Terms, Concept of Algorithm, Concept of Programming Languages and other Fundamentals of Programming:**

**🔗 [Visit the "Fundamentals_of_Programming" Repository](https://github.com/Muhammad-Hussain456/Fundamentals_of_Programming-)**

# 🐍 Python Fundamentals

## 📌 Program Structure  
Python programs are executed **line by line** starting from the top.  
پائتھن کا پروگرام اوپر سے نیچے کی طرف ایک لائن کے بعد دوسری لائن میں چلتا ہے۔

```python
# This is a comment
print("Hello, Python!")
```

### Constructs:

**Programming constructs** are the building blocks of a program. It’s important to know their **syntax, meaning (semantic)**, and how to use them in **examples**.

### 🔍 Syntax and Semantics

| Construct            | Syntax in Python           | Semantic in Python                                        | Example                                |
| -------------------- | -------------------------- | --------------------------------------------------------- | -------------------------------------- |
| Comment              | `# comment`                | Describes code; ignored by interpreter                    | `# This prints a message`              |
| Print Statement      | `print(value)`             | Displays value on screen                                  | `print("Hello")`                       |
| Main Entry (optional)| `if __name__ == "__main__"`| Optional main block to execute code when run as a script  | `if __name__ == "__main__": main()`    |

---

## 🧠 Variables

Variables are containers used to store data.
ویری ایبلز ڈیٹا محفوظ کرنے کے لیے استعمال ہوتے ہیں۔

```python
age = 25
height = 5.9
grade = 'A'
is_passed = True
```

### 🔍 Syntax and Semantics

| Construct               | Syntax in Python          | Semantic in Python                             | Example                                |
| ----------------------- | ------------------------- | ---------------------------------------------- | -------------------------------------- |
| Variable Initialization    | `variable = value`        | Creates a variable and assigns value           | `age = 25`                             |
| Dynamic Typing          | No explicit type needed   | Python figures out the type automatically      | `name = "Ali"`                         |
| Reassignment            | `variable = new_value`    | Updates the variable value                     | `age = 30`                             |

---

## 💡 Data Types and Range (حد)

Data types determine the kind of data a variable can hold.
ڈیٹا ٹائپ سے پتا چلتا ہے کہ ویری ایبل میں کس قسم کا ڈیٹا رکھا جا سکتا ہے۔

| Data Type | Example Values       | Description                          | Example Code             |
| --------- | -------------------- | ------------------------------------ | ------------------------ |
| `int`     | 10, -5, 200          | Whole numbers                        | `a = 100`                |
| `float`   | 3.14, -2.7           | Decimal numbers                      | `pi = 3.14`              |
| `str`     | "Ali", 'Hello'       | Sequence of characters (string)      | `name = "Ali"`           |
| `bool`    | `True`, `False`      | Logical values                       | `is_passed = True`       |
| `list`    | [1, 2, 3]            | Ordered collection of items          | `numbers = [1, 2, 3]`    |
| `dict`    | {"name": "Ali"}      | Key-value pairs                      | `info = {"age": 20}`     |

```python
marks = 85           # int
height = 5.9         # float
grade = 'A'          # str
passed = True        # bool
```

---

## 🎯 Input/Output Operations

**Input** takes data from the user.  
**Output** displays it on the screen.  
انپٹ یوزر سے ڈیٹا لیتا ہے، آؤٹ پٹ اسکرین پر دکھاتا ہے۔

```python
name = input("Enter your name: ")
print("Hello,", name)
```

### 🔍 Syntax and Semantics

| Construct   | Syntax in Python           | Semantic in Python                     | Example                           |
| ----------- | -------------------------- | -------------------------------------- | --------------------------------- |
| Output      | `print(value)`             | Displays a value on screen             | `print("Welcome")`               |
| Input       | `input(prompt)`            | Takes string input from user           | `age = input("Enter age: ")`     |
| Type Casting| `int(input())`, `float()`  | Converts input to int, float, etc.     | `age = int(input("Enter age: "))`|

---

## 🔄 Type Conversion

Type conversion changes data from one type to another.
کسی ڈیٹا کو ایک ٹائپ سے دوسری میں تبدیل کرنا۔

```python
a = 5
b = 2.0
c = a + b   # Implicit: int is converted to float
print(c)    # Output: 7.0

x = 5
y = float(x)      # Explicit
print(y)    # Output: 5.0

```

### 🔍 Syntax and Semantics

| Type                    | Syntax in Python               | Semantic in Python                           | Example                      |
| ----------------------- | ----------------------------- | --------------------------------------------- | ---------------------------- |
| Implicit Conversion     | `var1 = value, var2 = value; var3 = var1 operator var2`         | Python auto converts one data type to another during an operation — if needed                | `a = 5, b = 2.0, c = a + b   # Implicit: int is converted to float  `               |
| Explicit Conversion     | `var1 = int(var2)`    | Manually convert data type                    | `y = int(5.9)`               |

---

## 🧪 Example Program

### Problem

Create variables for student marks, height, grade, and pass status. Assign values and display them.

### Coding

```python
marks = 85
height = 5.9
grade = 'A'
passed = True

print("Marks:", marks)
print("Height:", height)
print("Grade:", grade)
print("Passed:", passed)
```

**Output**:

```
Marks: 85
Height: 5.9
Grade: A
Passed: True
```

---

## 🏗️ Program Execution Steps

1. **Parsing** – Python reads and parses the code line by line.
2. **Compilation (internally)** – Python compiles code into bytecode behind the scenes.
3. **Interpretation** – The Python interpreter runs bytecode line by line.
4. **Memory Management** – Variables and objects are stored in memory automatically.
5. **Execution** – Code runs from top to bottom unless controlled by conditions or loops.

---

> ✅ Python is dynamically typed, beginner-friendly, and used in everything from automation to AI.
