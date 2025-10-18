# 🧵 Strings in Python

---

## 📌 What Is a String?

A **string** in Python is a **sequence of characters** enclosed in **single quotes `' '`** or **double quotes `" "`** used to **represent text**.

Python provides a wide range of **built-in string methods** to perform operations such as concatenation, searching, and formatting.


---

### 🔍 Syntax and Semantics

| Construct              | Syntax in Python                     | Semantic in Python                                              | Example                                      |
|------------------------|--------------------------------------|-----------------------------------------------------------------|----------------------------------------------|
| String Declaration     | `variable = ""`                      | Declares an empty string variable                               | `msg = ""`                                  |
| String Initialization  | `variable = "text"`                  | Declares and assigns a string value                             | `name = "Ali"`                              |
| Multi-line String      | `''' text '''` or `""" text """`     | Used for multi-line string values                               | `msg = """Hello\nWorld"""`                  |
| String Concatenation   | `str1 + str2`                        | Joins two strings together                                      | `"Hello " + name`                           |
| String Input (single line) | `input("Prompt: ")`               | Reads input as a string (entire line)                           | `name = input("Enter your name: ")`         |
| String Output          | `print(variable)`                    | Displays string on screen                                       | `print(name)`                               |

---

### 🔍 Difference Between `input()` and Hardcoded Strings

| Feature / خصوصیت          | Hardcoded String (`name = "Ali"`)     | User Input (`input()`)                                  |
|---------------------------|---------------------------------------|----------------------------------------------------------|
| 📌 Purpose / مقصد          | Value is initialize in code           | Value is taken from the user at runtime                  |
| 🧠 Behavior                | No input required                     | Waits for user input                                    |
| 🧪 Example                 | `name = "Ali"`                        | `name = input("Enter your name: ")`                     |
| 📤 Output Example          | `print(name)` → `Ali`                 | User types → `Ali` → Printed output                     |
| ✅ Use Case / استعمال کب کریں | For testing or predefined data        | For user-interactive programs                            |

---

## 🧩 Example Problem 1  

Store a name and city in string variables and display them.  

---

## ✅ Problem Definition  

Create a simple program that uses two string variables to store two text values and prints them using `print()`.

---

## 🔍 Problem Analysis  
- Use variables `name` and `city` to store string data.  
- Assign values directly (hardcoded).  
- Display output using `print()`.

---

## 🧮 Algorithm  
1. Start the program  
2. Declare two string variables  
3. Assign string values to them  
4. Print both values using `print()`  
5. End the program  

---

## 💻 Program

```python
# Program to store and display name and city

name = "Muslim Ali"
city = "Skardu"

print("Full Name:", name)
print("City:", city)


---

🧪 Output

Full Name: Muslim Ali
City: Skardu


---

✅ Example Problem 2

Ask the user for their name and city, then display a welcome message.


---

🧩 Problem Definition

The program takes user input for their name and city and displays a personalized welcome message.


---

🔍 Problem Analysis

Use input() to take user input for both fields.

Combine strings using the + operator or commas in print().

Display output in a friendly message.



---

🧮 Algorithm

1. Start the program


2. Input user’s name


3. Input user’s city


4. Display a welcome message combining both


5. End the program




---

💻 Program

# Program to take user name and city as input and display message

full_name = input("Enter your full name: ")
city = input("Enter your city: ")

print("Welcome", full_name, "from", city + "!")


---

🧪 Sample Input

Enter your full name: Sartaj Ali
Enter your city: Skardu

📤 Output

Welcome Sartaj Ali from Skardu!


---

🧠 Key Points to Remember

Concept	Description	Example

Strings are immutable	You can’t change characters directly inside a string	❌ name[0] = 'A' (Error)
Use + for concatenation	Joins two or more strings	"Hello " + "World"
Use len() for length	Returns number of characters	len("Ali") → 3
Use f-string for formatting	Cleaner way to combine strings and variables	f"Welcome {name} from {city}!"



---

💡 Bonus Example (Using f-string)

full_name = input("Enter your full name: ")
city = input("Enter your city: ")

print(f"Welcome {full_name} from {city}!")

✅ Output:

Welcome Sartaj Ali from Skardu!


---
