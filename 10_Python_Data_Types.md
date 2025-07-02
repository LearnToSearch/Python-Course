# Data Types In Python 📊

**Python data types** in full detail. Data types define the kinds of values that can be stored and manipulated within a program. Python is a dynamically typed language, which means that you don't need to declare the type of a variable; the interpreter infers it at runtime. 🔍

---

## **1. Python Standard Data Types** 🗂️

Python supports the following standard data types:

1. **Numeric Types**: 🔢
   - `int` (Integer)
   - `float` (Floating-point number)
   - `complex` (Complex numbers)
2. **Sequence Types**: 📏
   - `str` (String)
   - `list` (List)
   - `tuple` (Tuple)
3. **Set Types**: 🔀
   - `set` (Set)
   - `frozenset` (Immutable Set)
4. **Mapping Type**: 📜
   - `dict` (Dictionary)
5. **Boolean Type**: ✅
   - `bool` (Boolean)
6. **Binary Types**: 💾
   - `bytes`
   - `bytearray`
   - `memoryview`
7. **None Type**: ❌
   - `NoneType` (Special data type for the absence of a value)

---

### **1. Numeric Types** 🔢

Python supports three distinct numeric types: **integers**, **floating-point numbers**, and **complex numbers**.

#### **a. Integer (`int`)**  🌟
- Integers are whole numbers (positive or negative) without a fractional part.
- In Python, integers have unlimited precision.

##### Example:
```python
a = 5      # Integer
b = -10    # Negative integer
print(type(a))  # Output: <class 'int'>
```

##### Operations:
- **Arithmetic**: Addition, subtraction, multiplication, division, modulus, exponentiation
- **Bitwise**: AND, OR, XOR, NOT, left shift, right shift

---

#### **b. Floating-point (`float`)** 🌊
- Floating-point numbers represent real numbers and are written with a decimal point.
- They can also be represented in scientific notation (e.g., `1.5e2` is equivalent to `150.0`).

##### Example:
```python
a = 5.5    # Float
b = 1.2e3  # Float (scientific notation)
print(type(a))  # Output: <class 'float'>
```

##### Operations:
- Supports all arithmetic operations: addition, subtraction, etc.

---

#### **c. Complex (`complex`)** 🔮
- Complex numbers are written as `a + bj`, where `a` is the real part and `b` is the imaginary part, and `j` is the imaginary unit (`√(-1)`).

##### Example:
```python
z = 3 + 4j  # Complex number
print(type(z))  # Output: <class 'complex'>
```

##### Operations:
- Supports addition, subtraction, multiplication, and division of complex numbers.

---

### **2. Sequence Types** 📏

Python has three main sequence types: **strings**, **lists**, and **tuples**. Sequences are ordered collections of items.

#### **a. String (`str`)** 📝
- Strings are immutable sequences of Unicode characters enclosed in single quotes (`'`) or double quotes (`"`).
- Python supports multi-line strings using triple quotes (`'''` or `"""`).

##### Example:
```python
s = "Hello, World!"  # String
multiline = '''This is
a multi-line
string.'''
print(type(s))  # Output: <class 'str'>
```

##### Operations:
- **Concatenation**: `+` (joins two strings)
- **Repetition**: `*` (repeats the string multiple times)
- **Indexing and slicing**: Access specific characters or substrings
- **Methods**: `upper()`, `lower()`, `strip()`, `split()`, etc.

##### Example of slicing:
```python
s = "Hello"
print(s[1:4])  # Output: "ell"
```

---

#### **b. List (`list`)** 🗒️
- Lists are ordered, mutable sequences of items.
- Lists can store elements of any data type, including other lists (nested lists).

##### Example:
```python
my_list = [1, 2, 3, "apple", [5, 6, 7]]  # List
print(type(my_list))  # Output: <class 'list'>
```

##### Operations:
- **Indexing and slicing**: Access individual elements or sublists.
- **List methods**: `append()`, `insert()`, `pop()`, `remove()`, `sort()`, etc.

##### Example of list method:
```python
my_list.append(10)  # Adds 10 to the end of the list
print(my_list)  # Output: [1, 2, 3, "apple", [5, 6, 7], 10]
```

---

#### **c. Tuple (`tuple`)** 📦
- Tuples are similar to lists, but they are immutable, meaning their elements cannot be changed after creation.
- Tuples are often used for fixed collections of items, like coordinates.

##### Example:
```python
my_tuple = (1, 2, 3, "apple")  # Tuple
print(type(my_tuple))  # Output: <class 'tuple'>
```

##### Operations:
- **Indexing and slicing**: Same as lists.
- **Immutability**: Once created, the elements in a tuple cannot be modified.

##### Example:
```python
print(my_tuple[1])  # Output: 2
```

---

### **3. Set Types** 🔀

Python includes two set types: **set** and **frozenset**. Sets are unordered collections of unique elements.

#### **a. Set (`set`)** 🆔
- A set is an unordered collection of unique items, meaning no duplicates.
- It is mutable (you can add or remove items).

##### Example:
```python
my_set = {1, 2, 3, 4, 4, 5}  # Set
print(my_set)  # Output: {1, 2, 3, 4, 5}
```

##### Operations:
- **Set operations**: Union (`|`), intersection (`&`), difference (`-`), symmetric difference (`^`).
- **Set methods**: `add()`, `remove()`, `clear()`, etc.

##### Example:
```python
my_set.add(6)
print(my_set)  # Output: {1, 2, 3, 4, 5, 6}
```

---

#### **b. Frozen Set (`frozenset`)** 🔒
- Frozensets are like sets but are immutable (cannot be changed after creation).

##### Example:
```python
my_frozenset = frozenset([1, 2, 3, 4])
print(type(my_frozenset))  # Output: <class 'frozenset'>
```

##### Operations:
- **Supports all set operations** but does not allow modification of elements.

---

### **4. Mapping Type: Dictionary (`dict`)** 📜

A **dictionary** is an unordered collection of key-value pairs, where keys must be unique and of an immutable type (e.g., strings, numbers), but values can be of any type.

##### Example:
```python
my_dict = {"name": "John", "age": 25, "city": "New York"}  # Dictionary
print(type(my_dict))  # Output: <class 'dict'>
```

##### Operations:
- **Accessing values by key**: `my_dict['name']` → Output: `John`
- **Methods**: `keys()`, `values()`, `items()`, `get()`, `pop()`, etc.

##### Example of method:
```python
my_dict["age"] = 26  # Modify value for key 'age'
my_dict.pop("city")  # Removes the key-value pair 'city'
print(my_dict)  # Output: {'name': 'John', 'age': 26}
```

---

### **5. Boolean Type (`bool`)** ✔️

Booleans represent one of two values: `True` or `False`.

##### Example:
```python
a = True
b = False
print(type(a))  # Output: <class 'bool'>
```

##### Operations:
- **Logical operations**: `and`, `or`, `not`
- **Comparison**: Equal (`==`), greater than (`>`), less than (`<`), etc.

##### Example:
```python
print(5 > 3)  # Output: True
print(5 == 3)  # Output: False
```

---

### **6. Binary Types** 💾

Python provides binary types to handle binary data: **bytes**, **bytearray**, and **memoryview**.

#### **a. Bytes (`bytes`)** 🖥️
- A bytes object is an immutable sequence of bytes (integers in the range 0-255).
- Useful for binary data such as images or encoded text.

##### Example:
```python
my_bytes = b'Hello'  # Bytes literal
print(type(my_bytes))  # Output: <class 'bytes'>
```

---

#### **b. Bytearray (`byte

array`)** 🔄
- A `bytearray` is similar to bytes but is mutable, meaning its elements can be changed.

##### Example:
```python
my_bytearray = bytearray(b'Hello')
my_bytearray[0] = 72  # Modify first byte
print(my_bytearray)  # Output: bytearray(b'Hello')
```

---

#### **c. Memoryview (`memoryview`)** 🔍
- A memoryview object allows you to access the internal data of an object that supports the buffer protocol, like `bytes` or `bytearray`, without copying it.

##### Example:
```python
my_bytes = b'abc'
view = memoryview(my_bytes)
print(view[0])  # Output: 97 (ASCII of 'a')
```

---

### **7. None Type (`NoneType`)** 🚫

`None` represents the absence of a value. It is often used to indicate "no value" or "null" in functions and variables.

##### Example:
```python
a = None
print(type(a))  # Output: <class 'NoneType'>
```

---

## **Type Conversion** 🔄

Python provides built-in functions to convert data types:
- `int()`, `float()`, `str()`, `list()`, `tuple()`, `set()`, `dict()`, etc.

##### Example of Type Conversion:
```python
a = "123"
b = int(a)  # Convert string to integer
print(b)  # Output: 123
```

---

## **Conclusion** 🎉

Python's data types are versatile and dynamic, allowing you to handle different kinds of data in an intuitive and efficient way. Understanding these types is essential for effective programming in Python.


