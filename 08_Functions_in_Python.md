# 🧠 Functions in Python

Functions are reusable blocks of code that perform a specific task. They help organize logic, reduce repetition, and improve readability.

---

## 🔧 Function Definition

### ✅ Syntax
```python
def function_name(parameters):
    # code block
    return result
```

### 📘 Semantic Meaning  
- `def` starts the function definition.
- `function_name` is the identifier.
- `parameters` are inputs (optional).
- `return` sends back a result (optional).

### 💡 Example
```python
def greet(name):
    return "Hello, " + name

print(greet("Muhammad"))  # Output: Hello, Muhammad
```

---

## 📥 Function Parameters

### ✅ Syntax
```python
def add(a, b):
    return a + b
```

### 📘 Semantic Meaning  
Parameters allow you to pass values into a function.

### 💡 Example
```python
print(add(5, 3))  # Output: 8
```

---

## 📤 Return Statement

### ✅ Syntax
```python
return value
```

### 📘 Semantic Meaning  
Returns a value from the function to the caller.

### 💡 Example
```python
def square(x):
    return x * x

result = square(4)
print(result)  # Output: 16
```

---

## 🧱 Function Without Parameters

### ✅ Syntax
```python
def say_hello():
    print("Hello!")
```

### 💡 Example
```python
say_hello()  # Output: Hello!
```

---

## 🧱 Function Without Return

### ✅ Syntax
```python
def show_message(msg):
    print(msg)
```

### 📘 Semantic Meaning  
Performs an action but does not return a value.

---

## 🔁 Calling a Function

### ✅ Syntax
```python
function_name(arguments)
```

### 💡 Example
```python
def multiply(a, b):
    return a * b

print(multiply(3, 4))  # Output: 12
```

---

## 🧩 Nested Functions (Optional)

### ✅ Syntax
```python
def outer():
    def inner():
        print("Inner function")
    inner()
```

### 💡 Example
```python
outer()  # Output: Inner function
```

---
