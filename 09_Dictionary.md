# 🔥 Dictionaries in Python

## 📚 Chapter 1: Python Dictionaries Overview

### What are Dictionaries?
**Dictionaries** are unordered collections of key-value pairs. They are mutable, dynamic, and extremely efficient for lookups.

### Real-Life Analogy: **School Student Database** 🏫
- **Dictionary** = Student records system
- **Keys** = Student ID numbers
- **Values** = Student information (name, grade, age)
- **Lookup** = Finding student by ID number

## 🏗️ Chapter 2: Dictionary Creation & Basics

### Creating Dictionaries
```python
# Empty dictionary
empty_dict = {}
empty_dict = dict()

# Dictionary with key-value pairs
student = {
    "name": "Muslim",
    "age": 16,
    "grade": 85.5,
    "subjects": ["Math", "Science", "English"]
}

school_records = {
    "STU001": {"name": "Muslim", "grade": 85},
    "STU002": {"name": "Sartaj", "grade": 92},
    "STU003": {"name": "Bilal", "grade": 78}
}

# Using dict() constructor
grades = dict(Math=85, Science=92, English=78)
colors = dict([("red", "#FF0000"), ("green", "#00FF00"), ("blue", "#0000FF")])
```

### Memory Visualization
```
school_records → [0x1000] → {
    "STU001": [0x2000] → {"name": "Muslim", "grade": 85},
    "STU002": [0x3000] → {"name": "Sartaj", "grade": 92},
    "STU003": [0x4000] → {"name": "Bilal", "grade": 78}
}
```

---

## 🔑 Chapter 3: Dictionary Operations & Accessing

### 1. Accessing Values
```python
student = {
    "name": "Muslim",
    "age": 16,
    "grade": 85.5,
    "school": "Skardu Public School"
}

# Access using square brackets
print(student["name"])   # "Muslim"
print(student["age"])    # 16

# Access using get() method (safer)
print(student.get("name"))          # "Muslim"
print(student.get("address"))       # None (key doesn't exist)
print(student.get("address", "Not provided"))  # "Not provided" (default value)

# Access all keys, values, and items
print(student.keys())    # dict_keys(['name', 'age', 'grade', 'school'])
print(student.values())  # dict_values(['Muslim', 16, 85.5, 'Skardu Public School'])
print(student.items())   # dict_items([('name', 'Muslim'), ('age', 16), ...])
```

### 2. Adding & Modifying Elements
```python
student = {"name": "Muslim", "age": 16}

# Adding new key-value pairs
student["grade"] = 85.5
student["school"] = "Skardu Public School"

# Modifying existing values
student["age"] = 17  # Update age

# Using update() to add multiple items
student.update({"subjects": ["Math", "Science"], "attendance": "95%"})

print(student)
# {'name': 'Muslim', 'age': 17, 'grade': 85.5, 'school': 'Skardu Public School', 
#  'subjects': ['Math', 'Science'], 'attendance': '95%'}
```

### 3. Removing Elements
```python
student = {
    "name": "Muslim",
    "age": 16,
    "grade": 85.5,
    "school": "Skardu Public School"
}

# Remove specific key
removed_grade = student.pop("grade")  # Returns 85.5 and removes key
removed_school = student.pop("school", "Unknown")  # With default value

# Remove last inserted item (Python 3.7+)
last_item = student.popitem()  # Returns ('age', 16) and removes it

# Remove all items
student.clear()  # Empty dictionary: {}

# Delete entire dictionary
del student  # Dictionary no longer exists
```

### 4. Checking Membership
```python
student = {"name": "Muslim", "age": 16, "grade": 85.5}

# Check if key exists
print("name" in student)     # True
print("address" in student)  # False
print("address" not in student)  # True

# Check if value exists (less common)
print("Muslim" in student.values())  # True
print(20 in student.values())        # False
```

---

## 📊 Chapter 4: Dictionary Methods

### Essential Methods
```python
student = {"name": "Muslim", "age": 16, "grade": 85.5}

# get() - Safe value retrieval
name = student.get("name")  # "Muslim"
address = student.get("address", "Not provided")  # "Not provided"

# setdefault() - Get value or set default if key doesn't exist
age = student.setdefault("age", 18)  # 16 (key exists)
city = student.setdefault("city", "Skardu")  # "Skardu" (new key added)

# copy() - Create a shallow copy
student_copy = student.copy()

# fromkeys() - Create dictionary from sequence
subjects = ["Math", "Science", "English"]
default_grades = dict.fromkeys(subjects, 0)  # {'Math': 0, 'Science': 0, 'English': 0}
```

### Iteration Methods
```python
student = {"name": "Muslim", "age": 16, "grade": 85.5}

# Iterate through keys
for key in student:
    print(f"Key: {key}")

for key in student.keys():
    print(f"Key: {key}")

# Iterate through values
for value in student.values():
    print(f"Value: {value}")

# Iterate through key-value pairs
for key, value in student.items():
    print(f"{key}: {value}")
```

---

## 🔄 Chapter 5: Dictionary Comprehensions

### Basic Dictionary Comprehensions
```python
# Traditional approach
squares = {}
for i in range(1, 6):
    squares[i] = i ** 2
# Result: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

# Dictionary comprehension (more Pythonic)
squares = {i: i**2 for i in range(1, 6)}
# Result: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}
```

### Advanced Comprehensions
```python
students = ["Muslim", "Sartaj", "Bilal", "Ahmed"]

# Create dictionary with default values
student_grades = {name: 0 for name in students}
# Result: {'Muslim': 0, 'Sartaj': 0, 'Bilal': 0, 'Ahmed': 0}

# With condition
passed_students = {name: grade for name, grade in student_grades.items() if grade >= 50}

# Transforming keys and values
student_data = {name.upper(): f"Grade: {grade}" for name, grade in student_grades.items()}
```

### Real-World Example: Student Management
```python
# Convert list of tuples to dictionary
student_records = [("STU001", "Muslim"), ("STU002", "Sartaj"), ("STU003", "Bilal")]
student_dict = {student_id: name for student_id, name in student_records}
# Result: {'STU001': 'Muslim', 'STU002': 'Sartaj', 'STU003': 'Bilal'}

# Create grade distribution
grades = [85, 92, 78, 85, 90, 92, 78, 85]
grade_count = {grade: grades.count(grade) for grade in set(grades)}
# Result: {85: 3, 92: 2, 78: 2, 90: 1}
```

---

## 🎯 Chapter 6: Nested Dictionaries

### Creating Nested Dictionaries
```python
# School database with nested dictionaries
school_database = {
    "STU001": {
        "personal_info": {
            "name": "Muslim",
            "age": 16,
            "address": "Skardu"
        },
        "academic_info": {
            "grade": 10,
            "subjects": ["Math", "Science", "English"],
            "grades": {"Math": 85, "Science": 92, "English": 78}
        }
    },
    "STU002": {
        "personal_info": {
            "name": "Sartaj",
            "age": 17,
            "address": "Skardu"
        },
        "academic_info": {
            "grade": 11,
            "subjects": ["Physics", "Chemistry", "Biology"],
            "grades": {"Physics": 88, "Chemistry": 95, "Biology": 90}
        }
    }
}
```

### Accessing Nested Data
```python
# Access nested values
muslim_name = school_database["STU001"]["personal_info"]["name"]  # "Muslim"
sartaj_math_grade = school_database["STU002"]["academic_info"]["grades"]["Physics"]  # 88

# Safe access with get()
address = school_database.get("STU001", {}).get("personal_info", {}).get("address", "Unknown")

# Modifying nested data
school_database["STU001"]["academic_info"]["grades"]["Math"] = 90  # Update grade
school_database["STU001"]["personal_info"]["phone"] = "123-456-7890"  # Add new field
```

### Iterating Through Nested Dictionaries
```python
def print_student_records(database):
    for student_id, student_data in database.items():
        print(f"\nStudent ID: {student_id}")
        print(f"Name: {student_data['personal_info']['name']}")
        print(f"Age: {student_data['personal_info']['age']}")
        print("Grades:")
        for subject, grade in student_data['academic_info']['grades'].items():
            print(f"  {subject}: {grade}")

print_student_records(school_database)
```

---

## 📈 Chapter 7: Dictionary vs Other Data Structures

### Dictionary vs List
```python
# List - ordered, indexed by position
students_list = ["Muslim", "Sartaj", "Bilal"]
print(students_list[0])  # "Muslim" - by position

# Dictionary - unordered, indexed by key
students_dict = {"STU001": "Muslim", "STU002": "Sartaj", "STU003": "Bilal"}
print(students_dict["STU001"])  # "Muslim" - by key
```

### Performance Comparison
```python
import time

# Large dataset
data_size = 100000

# List lookup (O(n) time)
large_list = list(range(data_size))

start = time.time()
99999 in large_list  # Worst case - check last element
end = time.time()
print(f"List lookup: {end - start:.6f} seconds")

# Dictionary lookup (O(1) time)
large_dict = {i: i for i in range(data_size)}

start = time.time()
99999 in large_dict  # Constant time lookup
end = time.time()
print(f"Dictionary lookup: {end - start:.6f} seconds")
```

### Comparison Table
| Feature | Dictionary | List | Tuple |
|---------|------------|------|-------|
| **Order** | Unordered (Python 3.7+: insertion order) | Ordered | Ordered |
| **Indexing** | By keys | By position | By position |
| **Mutability** | ✅ Mutable | ✅ Mutable | ❌ Immutable |
| **Lookup Speed** | O(1) - Very fast | O(n) - Slow | O(n) - Slow |
| **Use Cases** | Key-value mappings, records | Sequences, collections | Fixed data, constants |

---

## 💼 Chapter 8: Real-World Applications

### 1. Student Management System
```python
class StudentManager:
    def __init__(self):
        self.students = {}
        self.next_id = 1
    
    def add_student(self, name, age, grade):
        student_id = f"STU{self.next_id:03d}"
        self.students[student_id] = {
            "name": name,
            "age": age,
            "grade": grade,
            "subjects": {},
            "attendance": []
        }
        self.next_id += 1
        return student_id
    
    def add_grade(self, student_id, subject, grade):
        if student_id in self.students:
            self.students[student_id]["subjects"][subject] = grade
            return True
        return False
    
    def get_student_average(self, student_id):
        if student_id in self.students:
            grades = self.students[student_id]["subjects"].values()
            if grades:
                return sum(grades) / len(grades)
        return 0
    
    def display_student(self, student_id):
        student = self.students.get(student_id)
        if student:
            print(f"ID: {student_id}")
            print(f"Name: {student['name']}")
            print(f"Age: {student['age']}")
            print(f"Average Grade: {self.get_student_average(student_id):.2f}")
            print("Subjects:")
            for subject, grade in student["subjects"].items():
                print(f"  {subject}: {grade}")

# Usage
manager = StudentManager()
muslim_id = manager.add_student("Muslim", 16, 10)
sartaj_id = manager.add_student("Sartaj", 17, 11)

manager.add_grade(muslim_id, "Math", 85)
manager.add_grade(muslim_id, "Science", 92)
manager.add_grade(sartaj_id, "Physics", 88)

manager.display_student(muslim_id)
```

### 2. Configuration Management
```python
# Application configuration
APP_CONFIG = {
    "database": {
        "host": "localhost",
        "port": 5432,
        "name": "school_db",
        "user": "admin",
        "password": "secure_password"
    },
    "school": {
        "name": "Skardu Public School",
        "max_students_per_class": 30,
        "subjects": ["Math", "Science", "English", "History", "Art"]
    },
    "features": {
        "enable_notifications": True,
        "auto_backup": True,
        "dark_mode": False
    }
}

def get_database_url(config):
    db = config["database"]
    return f"postgresql://{db['user']}:{db['password']}@{db['host']}:{db['port']}/{db['name']}"

def is_feature_enabled(config, feature_name):
    return config["features"].get(feature_name, False)

# Usage
db_url = get_database_url(APP_CONFIG)
notifications_enabled = is_feature_enabled(APP_CONFIG, "enable_notifications")
```

### 3. Grade Analytics
```python
def analyze_class_performance(gradebook):
    """Analyze class performance from gradebook dictionary"""
    analysis = {
        "total_students": len(gradebook),
        "subject_averages": {},
        "grade_distribution": {"A": 0, "B": 0, "C": 0, "D": 0, "F": 0},
        "top_students": []
    }
    
    # Calculate subject averages
    subjects = set()
    for student in gradebook.values():
        subjects.update(student["grades"].keys())
    
    for subject in subjects:
        subject_grades = [s["grades"].get(subject, 0) for s in gradebook.values()]
        analysis["subject_averages"][subject] = sum(subject_grades) / len(subject_grades)
    
    # Grade distribution
    for student in gradebook.values():
        avg_grade = sum(student["grades"].values()) / len(student["grades"])
        if avg_grade >= 90:
            analysis["grade_distribution"]["A"] += 1
        elif avg_grade >= 80:
            analysis["grade_distribution"]["B"] += 1
        elif avg_grade >= 70:
            analysis["grade_distribution"]["C"] += 1
        elif avg_grade >= 60:
            analysis["grade_distribution"]["D"] += 1
        else:
            analysis["grade_distribution"]["F"] += 1
    
    # Top students
    student_averages = []
    for name, data in gradebook.items():
        avg = sum(data["grades"].values()) / len(data["grades"])
        student_averages.append((name, avg))
    
    analysis["top_students"] = sorted(student_averages, key=lambda x: x[1], reverse=True)[:3]
    
    return analysis

# Sample data
gradebook = {
    "Muslim": {"grades": {"Math": 85, "Science": 92, "English": 78}},
    "Sartaj": {"grades": {"Math": 95, "Science": 88, "English": 92}},
    "Bilal": {"grades": {"Math": 78, "Science": 85, "English": 80}},
    "Ahmed": {"grades": {"Math": 65, "Science": 70, "English": 75}}
}

results = analyze_class_performance(gradebook)
print(results)
```

---

## 💡 Chapter 9: Best Practices

### 1. **Use Descriptive Keys**
```python
# Good - clear and descriptive
student_data = {
    "student_name": "Muslim",
    "student_age": 16,
    "average_grade": 85.5
}

# Avoid - unclear keys
data = {
    "n": "Muslim",
    "a": 16,
    "g": 85.5
}
```

### 2. **Use get() for Safe Access**
```python
student = {"name": "Muslim", "age": 16}

# Safe way - won't raise KeyError
grade = student.get("grade", 0)  # Returns 0 if key doesn't exist

# Unsafe way - raises KeyError if key doesn't exist
# grade = student["grade"]  # ❌ KeyError if 'grade' doesn't exist
```

### 3. **Use Dictionary Comprehensions**
```python
# Instead of this:
squares = {}
for i in range(5):
    squares[i] = i ** 2

# Use this (more Pythonic):
squares = {i: i**2 for i in range(5)}
```

### 4. **Use setdefault() for Initialization**
```python
# Group students by grade
students = [
    {"name": "Muslim", "grade": 10},
    {"name": "Sartaj", "grade": 11},
    {"name": "Bilal", "grade": 10},
    {"name": "Ahmed", "grade": 11}
]

# Efficient grouping
students_by_grade = {}
for student in students:
    students_by_grade.setdefault(student["grade"], []).append(student["name"])

print(students_by_grade)
# {10: ['Muslim', 'Bilal'], 11: ['Sartaj', 'Ahmed']}
```

---

## 🚀 Chapter 10: Advanced Dictionary Techniques

### 1. **collections.defaultdict**
```python
from collections import defaultdict

# Automatically handle missing keys
gradebook = defaultdict(list)

# No need to check if key exists
gradebook["Math"].append(85)
gradebook["Science"].append(92)
gradebook["Math"].append(78)

print(dict(gradebook))
# {'Math': [85, 78], 'Science': [92]}

# With default factory
word_count = defaultdict(int)
for word in ["apple", "banana", "apple", "cherry"]:
    word_count[word] += 1

print(dict(word_count))  # {'apple': 2, 'banana': 1, 'cherry': 1}
```

### 2. **collections.OrderedDict**
```python
from collections import OrderedDict

# Maintains insertion order (Python 3.7+ regular dict also does this)
student_registry = OrderedDict()

student_registry["STU001"] = "Muslim"
student_registry["STU002"] = "Sartaj"
student_registry["STU003"] = "Bilal"

# Items are in insertion order
for student_id, name in student_registry.items():
    print(f"{student_id}: {name}")
```

### 3. **Merging Dictionaries**
```python
# Python 3.5+ - using ** unpacking
personal_info = {"name": "Muslim", "age": 16}
academic_info = {"grade": 10, "school": "Skardu Public School"}

student_data = {**personal_info, **academic_info}
# {'name': 'Muslim', 'age': 16, 'grade': 10, 'school': 'Skardu Public School'}

# Python 3.9+ - using | operator
student_data = personal_info | academic_info

# Using update()
student_data = personal_info.copy()
student_data.update(academic_info)
```

### 4. **Dictionary Views**
```python
student = {"name": "Muslim", "age": 16, "grade": 85.5}

# Dictionary views are dynamic
keys_view = student.keys()
values_view = student.values()
items_view = student.items()

print(keys_view)   # dict_keys(['name', 'age', 'grade'])

# Views update when dictionary changes
student["school"] = "Skardu Public School"
print(keys_view)   # dict_keys(['name', 'age', 'grade', 'school'])
```

---

## 📋 Chapter 11: Quick Reference Guide

### Dictionary Methods Cheat Sheet
```python
student = {"name": "Muslim", "age": 16}

# Adding/Updating
student["grade"] = 85.5                    # Add/update
student.update({"school": "SPS", "city": "Skardu"})  # Multiple updates
age = student.setdefault("age", 18)        # Get or set default

# Removing
grade = student.pop("grade")               # Remove and return
item = student.popitem()                   # Remove last item
student.clear()                            # Remove all items

# Accessing
name = student["name"]                     # Direct access
name = student.get("name")                 # Safe access
name = student.get("address", "Unknown")   # With default

# Information
keys = student.keys()                      # View of keys
values = student.values()                  # View of values  
items = student.items()                    # View of key-value pairs
length = len(student)                      # Number of items
exists = "name" in student                 # Check key existence
```

### Common Patterns
```python
# Counting with dictionaries
words = ["apple", "banana", "apple", "cherry", "banana", "apple"]
word_count = {}
for word in words:
    word_count[word] = word_count.get(word, 0) + 1

# Grouping with dictionaries
students = [("Muslim", 10), ("Sartaj", 11), ("Bilal", 10), ("Ahmed", 11)]
by_grade = {}
for name, grade in students:
    by_grade.setdefault(grade, []).append(name)

# Dictionary comprehension with condition
numbers = [1, 2, 3, 4, 5, 6]
even_squares = {x: x**2 for x in numbers if x % 2 == 0}
```

---

## 🎓 Chapter 12: Key Takeaways

### ✅ Dictionaries are POWERFUL:
- **Fast lookups** - O(1) time complexity
- **Flexible keys** - Almost any immutable type
- **Dynamic** - Easy to add, remove, modify
- **Versatile** - Perfect for records, configurations, mappings

### 🎯 Use Dictionaries for:
- **Key-value mappings** - Student records, configurations
- **Fast lookups** - When you need to find data quickly
- **Grouping data** - Categorizing and organizing information
- **JSON-like structures** - Nested data representations

### 🔥 Remember:
- **Keys must be immutable** (strings, numbers, tuples)
- **Use get() for safe access** to avoid KeyError
- **Dictionary comprehensions** are Pythonic and efficient
- **Nested dictionaries** are great for complex data
- **Choose dictionaries when you need fast lookups by key**

### 💡 Final Thought:
**Dictionaries in Python are like SMART PHONE CONTACTS:**
- **Keys** = Contact names
- **Values** = Contact information (phone, email, address)
- **Lookup** = Find contact by name (instant!)
- **Organization** = Group contacts by category

**Master dictionaries, and you'll handle complex data structures with ease!** 🐍✨

*Happy Coding!* 💻🚀
