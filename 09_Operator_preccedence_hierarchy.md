# 📊 Operator Precedence Hierarchy In Python :-

**Operator precedence** and **associativity** in Python define the order of operations when evaluating expressions. Operators with higher precedence are executed before those with lower precedence. **Associativity** determines how operators of the same precedence are grouped without parentheses (either left-to-right or right-to-left).

---

## **1. Python Operator Precedence Hierarchy**

Here’s the full precedence hierarchy from highest to lowest:

| Precedence | Operator                                                                                  | Description                                      | Associativity          |
|------------|-------------------------------------------------------------------------------------------|--------------------------------------------------|------------------------|
| **1**      | `()`                                                                                      | Parentheses (for grouping expressions)           | Left to right          |
| **2**      | `**`                                                                                      | Exponentiation                                   | Right to left          |
| **3**      | `+x`, `-x`, `~x`                                                                          | Unary plus, Unary minus, Bitwise NOT             | Right to left          |
| **4**      | `*`, `/`, `//`, `%`                                                                       | Multiplication, Division, Floor Division, Modulus| Left to right          |
| **5**      | `+`, `-`                                                                                  | Addition, Subtraction                            | Left to right          |
| **6**      | `<<`, `>>`                                                                                | Bitwise Shift operators                          | Left to right          |
| **7**      | `&`                                                                                       | Bitwise AND                                      | Left to right          |
| **8**      | `^`                                                                                       | Bitwise XOR                                      | Left to right          |
| **9**      | `|`                                                                                        | Bitwise OR                                       | Left to right          |
| **10**     | `in`, `not in`, `is`, `is not`, `<`, `<=`, `>`, `>=`, `!=`, `==`                       | Comparisons, Membership, Identity operators      | Left to right          |
| **11**     | `not`                                                                                     | Logical NOT                                      | Right to left          |
| **12**     | `and`                                                                                     | Logical AND                                      | Left to right          |
| **13**     | `or`                                                                                      | Logical OR                                       | Left to right          |
| **14**     | `if – else`                                                                               | Conditional (ternary) expression                 | Right to left          |
| **15**     | `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `//=`, `**=`, `&=`, `|=`, `^=`, `>>=`, `<<=`          | Assignment operators                             | Right to left          |
| **16**     | `,`                                                                                       | Comma (used in tuple unpacking and function arguments) | Left to right      |

---

## **2. Detailed Explanation of Each Precedence Level**

### **1. Parentheses `()`** 🟢
Parentheses have the highest precedence. Expressions within parentheses are evaluated first, allowing you to override the default precedence.

#### Example:
```python
result = (2 + 3) * 4  # Output: 20
```
- Without parentheses: `2 + 3 * 4 = 14`
- With parentheses: `(2 + 3) * 4 = 20`

---

### **2. Exponentiation `**`** 🔼
Exponentiation has the second-highest precedence and is right-associative, meaning that multiple exponentiation operations are evaluated from right to left.

#### Example:
```python
result = 2 ** 3 ** 2  # Output: 512
# Equivalent to: 2 ** (3 ** 2) = 2 ** 9 = 512
```

---

### **3. Unary Plus `+x`, Unary Minus `-x`, and Bitwise NOT `~x`** ➕➖
These operators act on a single operand and are evaluated next, right to left. Unary `+` returns the value unchanged, `-` negates the value, and `~` inverts all bits.

#### Example:
```python
result = -5 + 3  # Output: -2
result = ~4      # Output: -5 (inverts the bits of 4)
```

---

### **4. Multiplication `*`, Division `/`, Floor Division `//`, Modulus `%`** ➗
These operators are evaluated left to right and have the next highest precedence. They perform basic arithmetic operations on numbers.

#### Example:
```python
result = 10 * 3 / 2  # Output: 15.0
```
Python first multiplies `10 * 3 = 30`, then divides `30 / 2 = 15.0`.

---

### **5. Addition `+`, Subtraction `-`** ➕➖
Addition and subtraction also have left-to-right associativity and come after multiplication and division in precedence.

#### Example:
```python
result = 10 + 5 - 2  # Output: 13
# First 10 + 5 = 15, then 15 - 2 = 13
```

---

### **6. Bitwise Shift Operators `<<`, `>>`** ⬅️➡️
These operators shift the bits of a number to the left or right. Left shifts multiply by powers of 2, while right shifts divide by powers of 2.

#### Example:
```python
result = 5 << 1  # Output: 10 (equivalent to 5 * 2)
result = 5 >> 1  # Output: 2  (equivalent to 5 // 2)
```

---

### **7. Bitwise AND `&`** ✋
This operator performs a bitwise AND operation between corresponding bits of two numbers. Both bits must be `1` for the result to be `1`.

#### Example:
```python
result = 5 & 3  # Output: 1
# Binary: 5 = 0101, 3 = 0011 → Result = 0001 (1 in decimal)
```

---

### **8. Bitwise XOR `^`** ⚔️
This operator performs a bitwise XOR (exclusive OR) operation, which returns `1` only if the bits are different.

#### Example:
```python
result = 5 ^ 3  # Output: 6
# Binary: 5 = 0101, 3 = 0011 → Result = 0110 (6 in decimal)
```

---

### **9. Bitwise OR `|`** ✨
This operator performs a bitwise OR operation between corresponding bits of two numbers. If either bit is `1`, the result is `1`.

#### Example:
```python
result = 5 | 3  # Output: 7
# Binary: 5 = 0101, 3 = 0011 → Result = 0111 (7 in decimal)
```

---

### **10. Comparisons (`<`, `<=`, `>`, `>=`, `==`, `!=`), Membership (`in`, `not in`), Identity (`is`, `is not`)** ⚖️
These operators are used for comparing values, checking membership in sequences, and comparing object identities.

#### Example:
```python
print(5 < 10)    # True
print(5 == 5)    # True
print(5 is 5)    # True
print(5 in [1, 2, 5])  # True
```

---

### **11. Logical NOT `not`** ❌
Logical NOT has right-to-left associativity. It negates the truth value of its operand.

#### Example:
```python
result = not (5 > 3)  # Output: False
# Since 5 > 3 is True, `not` negates it to False
```

---

### **12. Logical AND `and`** 🔗
Logical AND returns `True` if both operands are true. It is evaluated left to right.

#### Example:
```python
result = (5 > 3) and (10 > 5)  # Output: True
```

---

### **13. Logical OR `or`** 🔄
Logical OR returns `True` if at least one operand is true. It also evaluates left to right.

#### Example:
```python
result = (5 < 3) or (10 > 5)  # Output: True
```

---

### **14. Conditional Expression (Ternary) `a if condition else b`** 🎭
The conditional (ternary) operator allows for conditional expressions in a single line and has right-to-left associativity.

#### Example:
```python
result = "Adult" if age >= 18 else "Minor"
```

---

### **15. Assignment Operators `=`, `+=`, `-=`, etc.** 💼
Assignment operators assign values to variables. Compound assignment operators like `+=` combine an arithmetic operation with assignment. They are evaluated right to left.

#### Example:
```python
a = 5
a += 3  # Equivalent to: a = a + 3 → a = 8
```

---

### **16. Comma `,`** 🗒️
The comma operator is used to separate expressions, such as in tuple unpacking or passing multiple arguments to a function.

#### Example:
```python
a, b = 5, 10  # Tuple unpacking
print(a, b)   # Output: 5 10
```

---

Here’s the section on operator precedence with emojis added for a more engaging presentation:

---

## **3. How Operator Precedence Works** 🧮

When evaluating an expression, Python first evaluates operators with higher precedence. If multiple operators have the same precedence, the associativity determines the order of operations.

### **Example of Precedence and Associativity:**
```python
result = 10 + 3 * 2 ** 2  # Output: 22
```
1. **Exponentiation (`**`)** has the highest precedence: 
   - \(2 ** 2 = 4\) 🔼
2. **Multiplication (`*`)** comes next: 
   - \(3 * 4 = 12\) ✖️
3. **Addition (`+`)** comes last: 
   - \(10 + 12 = 22\) ➕

---

## **Summary** 📚
- Operators with **higher precedence** are evaluated first. ⏳
- Operators with the **same precedence** are evaluated based on their **associativity** (left-to-right or right-to-left). ↔️
- Parentheses `()` can be used to explicitly control the order of evaluation. 🟡


