# Data Structures:

## **Classification Across Four Dimensions**

1. **Organization** (Linear vs Non-linear)
2. **Data Type** (Homogeneous vs Heterogeneous)
3. **Mutability** (Static vs Dynamic)
4. **Access Pattern** (Sequential vs Direct/Random vs Indexed)


---

## **DIMENSION 1: ORGANIZATION**

### **1.1 LINEAR STRUCTURES**
Elements arranged in a sequence, one after another.

**Examples:**
- Arrays, Lists, Stacks, Queues, Linked Lists, Vectors, Deques

### **1.2 NON-LINEAR STRUCTURES**
Elements form hierarchical or network relationships.

**Examples:**
- Trees, Graphs, Heaps, Hash Tables, Sets, Matrices

---

## **DIMENSION 2: DATA TYPE**

### **2.1 HOMOGENEOUS**
All elements are of the same type.

**Examples:**
- Arrays of integers, Lists of strings, Trees of floats

### **2.2 HETEROGENEOUS**
Elements can be of different types.

**Examples:**
- Python lists, JavaScript arrays, Tuples, Structs/Objects

---

## **DIMENSION 3: MUTABILITY**

### **3.1 STATIC**
Fixed size/content after creation (compile-time or initialization).

**Examples:**
- Static arrays, Fixed-size buffers, Immutable strings

### **3.2 DYNAMIC**
Can grow, shrink, or change during runtime.

**Examples:**
- Lists, Dynamic arrays, Trees, Graphs

---

## **DIMENSION 4: ACCESS PATTERN**

### **4.1 SEQUENTIAL ACCESS**
Must traverse elements in order to reach a specific element.

**Examples:**
- Linked lists, Tapes, Streams

### **4.2 DIRECT/RANDOM ACCESS**
Can jump directly to any element using an index/address.

**Examples:**
- Arrays, Vectors, Memory buffers

### **4.3 INDEXED ACCESS**
Access elements via keys/indices (not necessarily numeric).

**Examples:**
- Dictionaries, Hash maps, Databases, Associative arrays

---

## **COMPLETE PRACTICAL CLASSIFICATION**

### **A. LINEAR STRUCTURES**

#### **A1. Linear-Homogeneous-Static**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | Read-only linked list | C | `const struct Node* head;` |
| **Direct** | Static array | C/C++ | `int arr[100];` |
| **Indexed** | Enum array | C | `Color colors[MAX];` |

#### **A2. Linear-Homogeneous-Dynamic**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | Linked list | All | `LinkedList<Integer>` |
| **Direct** | Dynamic array/Vector | C++/Java | `vector<int>`, `ArrayList<Integer>` |
| **Indexed** | Growable array with named indices | Custom | `IndexedArray` class |

#### **A3. Linear-Heterogeneous-Static**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | Fixed tuple (immutable) | Python | `(1, "a", 3.14)` |
| **Direct** | Struct/Record | C/Go | `struct Person {int age; char* name;};` |
| **Indexed** | Fixed JSON/configuration | JSON | `{"name": "Alice", "age": 30}` |

#### **A4. Linear-Heterogeneous-Dynamic**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | Python list (used as queue) | Python | `[1, "hi", 3.14]` |
| **Direct** | Python list (index access) | Python | `lst[2] = "new"` |
| **Indexed** | JavaScript array | JS | `arr["property"] = value` |

---

### **B. NON-LINEAR STRUCTURES**

#### **B1. Non-linear-Homogeneous-Static**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | Fixed tree (ROM) | Embedded C | `const TreeNode tree;` |
| **Direct** | Precomputed lookup table | C | `int table[10][10];` |
| **Indexed** | Static hash table | C | `static KeyValue pairs[100];` |

#### **B2. Non-linear-Homogeneous-Dynamic**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | Tree traversal | All | `tree.inorder()` |
| **Direct** | Graph with node IDs | All | `graph.nodes[5]` |
| **Indexed** | Dictionary with string keys | C# | `Dictionary<string, int>` |

#### **B3. Non-linear-Heterogeneous-Static**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | XML/JSON template | XML/JSON | `<person><name>Alice</name><age>30</age></person>` |
| **Direct** | Compile-time expression tree | Compilers | `ASTNode* root;` |
| **Indexed** | Configuration file | YAML/TOML | `user.name = "Alice"` |

#### **B4. Non-linear-Heterogeneous-Dynamic**
| Access Pattern | Example | Language | Code |
|----------------|---------|----------|------|
| **Sequential** | DOM tree traversal | JavaScript | `document.body.childNodes` |
| **Direct** | Object graph with references | Python | `obj.attribute.subattribute` |
| **Indexed** | Database/NoSQL store | MongoDB | `db.users.findOne({name: "Alice"})` |

---

## **PYTHON EXAMPLES FOR ALL CATEGORIES**

```python
# A1. Linear-Homogeneous-Static-Direct
import array
static_arr = array.array('i', [1, 2, 3])  # Fixed type, direct access

# A2. Linear-Homogeneous-Dynamic-Sequential
class LinkedList:
    class Node:
        def __init__(self, data):
            self.data = data  # Assume same type
            self.next = None

# A3. Linear-Heterogeneous-Static-Indexed
from collections import namedtuple
Person = namedtuple('Person', ['name', 'age', 'height'])
alice = Person("Alice", 30, 165.5)  # Immutable, mixed types

# A4. Linear-Heterogeneous-Dynamic-Direct
python_list = [1, "hello", 3.14, [1, 2, 3]]  # Dynamic, mixed types
python_list[1] = "world"  # Direct access

# B1. Non-linear-Homogeneous-Static (simulated)
class StaticBinaryTree:
    # Pre-defined structure
    LEFT = 0
    RIGHT = 1
    tree = [
        [1, 2],   # Node 0: left=1, right=2
        [3, 4],   # Node 1
        [5, 6],   # Node 2
        [-1, -1], # Node 3 (leaf)
        [-1, -1], # Node 4 (leaf)
        [-1, -1], # Node 5 (leaf)
        [-1, -1]  # Node 6 (leaf)
    ]

# B2. Non-linear-Homogeneous-Dynamic-Direct
class TreeNode:
    def __init__(self, val):
        self.val = val  # All nodes store same type
        self.left = None
        self.right = None

# B3. Non-linear-Heterogeneous-Static (JSON)
import json
config = json.loads('{"app": "MyApp", "version": 1.0, "features": ["auth", "db"]}')
# Parsed but treated as static

# B4. Non-linear-Heterogeneous-Dynamic-Indexed
class GraphNode:
    def __init__(self, data):
        self.data = data  # Can be any type
        self.neighbors = []
        self.attributes = {}

# Create heterogeneous graph
graph = {
    "users": [
        {"id": 1, "name": "Alice", "age": 30},
        {"id": 2, "name": "Bob", "active": True}
    ],
    "connections": [
        {"from": 1, "to": 2, "type": "friend"}
    ]
}
```

---

## **C++ EXAMPLES**

```cpp
// A1. Linear-Homogeneous-Static-Direct
int staticArray[100];  // Direct access: staticArray[50]

// A2. Linear-Homogeneous-Dynamic-Sequential
#include <list>
std::list<int> linkedList;  // Sequential access

// A3. Linear-Heterogeneous-Static-Indexed
struct Person {
    std::string name;
    int age;
    double height;
};
Person people[10];  // Static array of structs

// A4. Linear-Heterogeneous-Dynamic (C++17+)
#include <any>
#include <vector>
std::vector<std::any> mixedVector;
mixedVector.push_back(42);
mixedVector.push_back("hello");
mixedVector.push_back(3.14);

// B2. Non-linear-Homogeneous-Dynamic-Indexed
#include <map>
std::map<std::string, int> dictionary;
dictionary["apple"] = 3;
dictionary["banana"] = 5;

// B4. Non-linear-Heterogeneous-Dynamic
#include <unordered_map>
#include <variant>
using JsonValue = std::variant<int, double, std::string, bool>;
std::unordered_map<std::string, JsonValue> jsonObject;
jsonObject["name"] = "Alice";
jsonObject["age"] = 30;
jsonObject["active"] = true;
```

---

## **PRACTICAL APPLICATIONS MATRIX**

| Use Case | Recommended Structure | Why |
|----------|---------------------|------|
| **Fixed-size buffer** | Linear-Homogeneous-Static-Direct | Memory efficiency, speed |
| **Shopping cart** | Linear-Heterogeneous-Dynamic-Sequential | Mixed items, changes often |
| **Database table** | Linear-Homogeneous-Dynamic-Indexed | Same type rows, key access |
| **File system** | Non-linear-Heterogeneous-Dynamic-Indexed | Mixed file types, hierarchical |
| **Social network** | Non-linear-Homogeneous-Dynamic | Nodes (users), edges (relationships) |
| **Compiler AST** | Non-linear-Heterogeneous-Static | Mixed node types, immutable |
| **Cache/LRU** | Linear-Homogeneous-Dynamic-Sequential | Fixed eviction order |
| **Configuration** | Non-linear-Heterogeneous-Static-Indexed | Mixed types, read-only |

---

## **MEMORY & PERFORMANCE CHARACTERISTICS**

| Category | Memory Overhead | Access Speed | Use When |
|----------|----------------|--------------|----------|
| **Linear-Static** | Low | Very Fast | Size known, type fixed |
| **Linear-Dynamic** | Medium | Fast | Size changes, type fixed |
| **Non-linear-Static** | Medium | Fast | Structure known |
| **Non-linear-Dynamic** | High | Medium | Complex relationships |
| **Homogeneous** | Low | Fast | Operations on same type |
| **Heterogeneous** | High | Slow | Need flexibility |

---

## **CHOOSING THE RIGHT STRUCTURE: DECISION TREE**

```
Start → Do elements form hierarchy/network?
    ├── No (Linear) → Is size fixed?
    │       ├── Yes → Are all elements same type?
    │       │       ├── Yes → Use Linear-Homogeneous-Static (Array)
    │       │       └── No → Use Linear-Heterogeneous-Static (Struct/Tuple)
    │       └── No → Need direct access?
    │               ├── Yes → Use Linear-Homogeneous-Dynamic (Vector/ArrayList)
    │               └── No → Use Linear-Heterogeneous-Dynamic (Python list)
    │
    └── Yes (Non-linear) → Is structure read-only?
            ├── Yes → Use Non-linear-Heterogeneous-Static (JSON/XML)
            └── No → Need key-based access?
                    ├── Yes → Use Non-linear-Heterogeneous-Dynamic-Indexed (Dict/Map)
                    └── No → Use Non-linear-Homogeneous-Dynamic (Tree/Graph)
```

---

## **SUMMARY**

1. **16 theoretical combinations** exist from 4 binary dimensions
2. **All are possible** in theory, but some are rare in practice
3. **Most common combinations:**
   - Linear-Homogeneous-Dynamic-Direct (Arrays/Lists)
   - Linear-Heterogeneous-Dynamic-Direct (Python/JS arrays)
   - Non-linear-Heterogeneous-Dynamic-Indexed (Dictionaries/Objects)
   - Non-linear-Homogeneous-Dynamic (Trees/Graphs)

4. **Language determines availability:**
   - **C/Java**: Strong on homogeneous, static structures
   - **Python/JavaScript**: Strong on heterogeneous, dynamic structures
   - **Modern languages**: Support all with varying efficiency

5. **Key insight**: Access pattern often depends on **implementation**, not just abstract type. A hash table provides indexed access but internally uses direct access.

