# Python Operators :-

## **1. What is an Operator?** 

An **operator** is a symbol or function that performs an operation on variables and values. In Python, operators are used to manipulate data and variables. Python supports a variety of operators, which can be grouped into several categories.

---

## **2. Types of Operators in Python**
1. **Arithmetic Operators** ➕
2. **Assignment Operators**✏️
3. **Comparison Operators** ⚖️
4. **Logical Operators** 🔗
5. **Bitwise Operators** 💻
6. **Membership Operators** 🔍
7. **Identity Operators** 🆔
8. **Special Operators (Ternary/Conditional Operator)** ❓

---

## **1. Arithmetic Operators** ➕
Arithmetic operators are used to perform mathematical operations such as addition, subtraction, multiplication, and division.

| Operator | Description           | Example      |
|----------|-----------------------|--------------|
| `+`      | Addition              | `a + b`      |
| `-`      | Subtraction           | `a - b`      |
| `*`      | Multiplication        | `a * b`      |
| `/`      | Division (float)      | `a / b`      |
| `//`     | Floor Division        | `a // b`     |
| `%`      | Modulus (remainder)   | `a % b`      |
| `**`     | Exponentiation        | `a ** b`     |

### **Explanation with Examples:**
```python
a = 15
b = 4

print(a + b)    # Addition: 15 + 4 = 19
print(a - b)    # Subtraction: 15 - 4 = 11
print(a * b)    # Multiplication: 15 * 4 = 60
print(a / b)    # Division: 15 / 4 = 3.75 (float division)
print(a // b)   # Floor Division: 15 // 4 = 3 (removes decimal part)
print(a % b)    # Modulus: 15 % 4 = 3 (remainder of the division)
print(a ** b)   # Exponentiation: 15 ** 4 = 50625 (15 to the power of 4)
```

---

## **2. Assignment Operators** ✏️
Assignment operators are used to assign values to variables. In addition to simple assignment (`=`), there are compound operators that combine an arithmetic operation with assignment.

| Operator | Description             | Example    |
|----------|-------------------------|------------|
| `=`      | Assign value            | `a = 5`    |
| `+=`     | Add and assign          | `a += 5`   |
| `-=`     | Subtract and assign     | `a -= 5`   |
| `*=`     | Multiply and assign     | `a *= 5`   |
| `/=`     | Divide and assign       | `a /= 5`   |
| `%=`     | Modulus and assign      | `a %= 5`   |
| `//=`    | Floor divide and assign | `a //= 5`  |
| `**=`    | Exponent and assign     | `a **= 5`  |

### **Explanation with Examples:**
```python
a = 10
a += 5  # a = a + 5 => 10 + 5 = 15
print(a)  # 15

a *= 2  # a = a * 2 => 15 * 2 = 30
print(a)  # 30

a //= 3  # a = a // 3 => 30 // 3 = 10
print(a)  # 10
```

---

## **3. Comparison Operators** ⚖️
Comparison operators are used to compare two values. They return either `True` or `False` depending on the condition.

| Operator | Description                  | Example      |
|----------|------------------------------|--------------|
| `==`     | Equal to                     | `a == b`     |
| `!=`     | Not equal to                 | `a != b`     |
| `>`      | Greater than                 | `a > b`      |
| `<`      | Less than                    | `a < b`      |
| `>=`     | Greater than or equal to     | `a >= b`     |
| `<=`     | Less than or equal to        | `a <= b`     |

### **Explanation with Examples:**
```python
a = 5
b = 3

print(a == b)   # False, because 5 is not equal to 3
print(a != b)   # True, because 5 is not equal to 3
print(a > b)    # True, because 5 is greater than 3
print(a < b)    # False, because 5 is not less than 3
print(a >= b)   # True, because 5 is greater than or equal to 3
print(a <= b)   # False, because 5 is not less than or equal to 3
```

---

## **4. Logical Operators** 🔗
Logical operators are used to combine conditional statements. They operate on boolean values (`True` or `False`).

| Operator | Description        | Example           |
|----------|--------------------|-------------------|
| `and`    | Returns `True` if both operands are `True` | `a and b` |
| `or`     | Returns `True` if at least one operand is `True` | `a or b`  |
| `not`    | Reverses the Boolean value of the operand | `not a`  |

### **Explanation with Examples:**
```python
a = True
b = False

print(a and b)   # False, because both are not True
print(a or b)    # True, because at least one is True
print(not a)     # False, because `not` reverses True to False
```

---

## **5. Bitwise Operators** 💻
Bitwise operators perform bit-level operations on integers. These operators treat numbers as binary (bit strings).

| Operator | Description                  | Example        |
|----------|------------------------------|----------------|
| `&`      | Bitwise AND                  | `a & b`        |
| `|`      | Bitwise OR                   | `a | b`        |
| `^`      | Bitwise XOR                  | `a ^ b`        |
| `~`      | Bitwise NOT                  | `~a`           |
| `<<`     | Left shift                   | `a << b`       |
| `>>`     | Right shift                  | `a >> b`       |

### **Explanation with Examples:**
```python
a = 10  # Binary: 1010
b = 4   # Binary: 0100

print(a & b)    # 0 (1010 & 0100 = 0000)
print(a | b)    # 14 (1010 | 0100 = 1110)
print(a ^ b)    # 14 (1010 ^ 0100 = 1110)
print(~a)       # -11 (inverts all the bits of 10)
print(a << 1)   # 20 (shift left: 1010 << 1 = 10100)
print(a >> 1)   # 5 (shift right: 1010 >> 1 = 0101)
```

---

## **6. Membership Operators** 🔍
Membership operators check for membership in a sequence (e.g., lists, strings, or tuples).

| Operator | Description             | Example         |
|----------|-------------------------|-----------------|
| `in`     | Returns `True` if a value exists in the sequence | `x in y` |
| `not in` | Returns `True` if a value does not exist in the sequence | `x not in y` |

### **Explanation with Examples:**
```python
fruits = ["apple", "banana", "cherry"]

print("apple" in fruits)    # True
print("grape" not in fruits) # True
```

---

## **7. Identity Operators** 🆔
Identity operators compare the memory location of two objects (i.e., if they are the same object).

| Operator | Description                   | Example       |
|----------|-------------------------------|---------------|
| `is`     | Returns `True` if both variables refer to the same object | `a is b` |
| `is not` | Returns `True` if both variables do not refer to the same object | `a is not b` |

### **Explanation with Examples:**
```python
a = [1, 2, 3]
b = [1, 2, 3]
c = a

print(a is b)     # False, because they are different objects
print(a is c)     # True, because they are the same object
print(a is not b) # True
```

---

## **8. Special Operators (Ternary/Conditional Operator)** ❓
This is a shorthand way of writing an `if-else` condition in a single line.

#### Syntax:
```python
result = value_if_true if condition else value_if_false
```

### **Explanation with Example:**
```python
age = 18
status = "Adult" if age >= 18 else "Minor"
print(status)  # Output: Adult
```

---

## **Summary of Python Operators:**
- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `//`, `%`, `**`
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=`
- **Comparison Operators**: `==

`, `!=`, `>`, `<`, `>=`, `<=`
- **Logical Operators**: `and`, `or`, `not`
- **Bitwise Operators**: `&`, `|`, `^`, `~`, `<<`, `>>`
- **Membership Operators**: `in`, `not in`
- **Identity Operators**: `is`, `is not`
- **Special Operators**: Ternary operator: `a if condition else b`


