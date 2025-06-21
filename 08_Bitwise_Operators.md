# Bitwise Operators

## **Bitwise Operators Overview**
Bitwise operators are used to manipulate individual bits of numbers. They treat numbers as sequences of binary digits (bits) and operate on them bit by bit.

Here are the **bitwise operators** in Python:

| Operator | Name               | Description |
|----------|--------------------|-------------|
| `&`      | AND                | Sets each bit to 1 if both bits are 1 |
| `|`      | OR                 | Sets each bit to 1 if one of the bits is 1 |
| `^`      | XOR (exclusive OR)  | Sets each bit to 1 if only one of the bits is 1 |
| `~`      | NOT                | Inverts all the bits (1’s complement) |
| `<<`     | Left Shift         | Shifts bits to the left by the given number of positions |
| `>>`     | Right Shift        | Shifts bits to the right by the given number of positions |

### Binary Numbers Basics
Binary is a base-2 number system. In binary, each digit is either `0` or `1`. Here's a refresher on how numbers are represented in binary:
- `5` in binary: `00000101`
- `9` in binary: `00001001`

Each bit represents an increasing power of 2, from right to left (2⁰, 2¹, 2², etc.).

---

### **1. Bitwise AND (`&`)**

The **AND** operator compares each bit of two numbers and returns `1` only if both corresponding bits are `1`. Otherwise, it returns `0`.

#### Truth Table:
| A   | B   | A & B |
|-----|-----|-------|
| 0   | 0   | 0     |
| 0   | 1   | 0     |
| 1   | 0   | 0     |
| 1   | 1   | 1     |

#### Example:
```python
a = 5      # Binary: 00000101
b = 3      # Binary: 00000011
result = a & b
print(result)  # Output: 1, which is binary 00000001
```
**Explanation**:
- `5 = 00000101`
- `3 = 00000011`
- `a & b = 00000001` (only the last bit is `1` in both numbers)

---

### **2. Bitwise OR (`|`)**

The **OR** operator compares each bit of two numbers and returns `1` if either of the corresponding bits is `1`. If both bits are `0`, it returns `0`.

#### Truth Table:
| A   | B   | A \| B |
|-----|-----|--------|
| 0   | 0   | 0      |
| 0   | 1   | 1      |
| 1   | 0   | 1      |
| 1   | 1   | 1      |

#### Example:
```python
a = 5      # Binary: 00000101
b = 3      # Binary: 00000011
result = a | b
print(result)  # Output: 7, which is binary 00000111
```
**Explanation**:
- `5 = 00000101`
- `3 = 00000011`
- `a | b = 00000111` (all bits where at least one is `1` become `1`)

---

### **3. Bitwise XOR (`^`)**

The **XOR (exclusive OR)** operator compares each bit of two numbers and returns `1` only if the corresponding bits are different (one is `0` and the other is `1`).

#### Truth Table:
| A   | B   | A ^ B |
|-----|-----|-------|
| 0   | 0   | 0     |
| 0   | 1   | 1     |
| 1   | 0   | 1     |
| 1   | 1   | 0     |

#### Example:
```python
a = 5      # Binary: 00000101
b = 3      # Binary: 00000011
result = a ^ b
print(result)  # Output: 6, which is binary 00000110
```
**Explanation**:
- `5 = 00000101`
- `3 = 00000011`
- `a ^ b = 00000110` (bits are `1` where they differ)

---

### **4. Bitwise NOT (`~`)**

The **NOT** operator inverts all the bits of a number, changing `0` to `1` and `1` to `0`. It returns the **complement** of the number. In Python, the bitwise NOT operator works as `-(x + 1)` due to the way negative numbers are stored in memory (using 2’s complement representation).

#### Example:
```python
a = 5      # Binary: 00000101
result = ~a
print(result)  # Output: -6, which is binary: 11111010 in 2’s complement
```
**Explanation**:
- `5 = 00000101`
- `~5 = -(5 + 1) = -6`
- In binary: `5 = 00000101` → `~5 = 11111010` (inverts all bits and represents it in two’s complement)

---

### **5. Left Shift (`<<`)**

The **left shift** operator shifts the bits of the number to the left by the specified number of positions, effectively multiplying the number by `2^n`, where `n` is the number of positions shifted.

#### Example:
```python
a = 5      # Binary: 00000101
result = a << 1
print(result)  # Output: 10, which is binary 00001010
```
**Explanation**:
- `5 = 00000101`
- `5 << 1` shifts all bits to the left by one position: `00001010` (equivalent to multiplying by 2)
- `a << 1 = 10`

#### Another Example:
```python
a = 5      # Binary: 00000101
result = a << 2
print(result)  # Output: 20, which is binary 00010100
```
- Shifting `5` two positions to the left: `00010100` (equivalent to multiplying by 4)

---

### **6. Right Shift (`>>`)**

The **right shift** operator shifts the bits of the number to the right by the specified number of positions, effectively dividing the number by `2^n`, where `n` is the number of positions shifted. The rightmost bits are discarded, and the leftmost bits are filled with `0` (for positive numbers).

#### Example:
```python
a = 20      # Binary: 00010100
result = a >> 1
print(result)  # Output: 10, which is binary 00001010
```
**Explanation**:
- `20 = 00010100`
- `20 >> 1` shifts all bits to the right by one position: `00001010` (equivalent to dividing by 2)
- `a >> 1 = 10`

#### Another Example:
```python
a = 20      # Binary: 00010100
result = a >> 2
print(result)  # Output: 5, which is binary 00000101
```
- Shifting `20` two positions to the right: `00000101` (equivalent to dividing by 4)

---

### **Combining Bitwise Operators**

You can combine multiple bitwise operators in a single operation to perform complex manipulations.

#### Example:
```python
a = 6       # Binary: 00000110
b = 3       # Binary: 00000011

result = (a | b) ^ (~b)
print(result)  # Output: -6
```

**Explanation**:
- `a | b = 00000111` (OR between `6` and `3`)
- `~b = 11111100` (NOT of `3`)
- `(a | b) ^ (~b)` = `00000111 ^ 11111100 = -6`

---

### **Practical Use Cases of Bitwise Operators**
1. **Setting and Clearing Specific Bits**: In system-level programming, bitwise operators are used to manipulate specific bits within a bitmask.
2. **Encryption**: XOR (`^`) is used in cryptography for encrypting data.
3. **Optimization in Code**: Bitwise operators are used in performance-critical code, such as for efficient multiplication, division, and toggling of bits.
4. **Graphics and Image Processing**: Bitwise operators are used to manipulate pixel data.

---

## **Summary of Bitwise Operators:**
- **`&` (AND)**: Compares each bit of two numbers and returns `1` if both bits are `1`.
- **`|` (OR)**: Compares each bit of two numbers and returns `1` if at least one bit is `1`.
- **`

^` (XOR)**: Compares each bit of two numbers and returns `1` if the bits are different.
- **`~` (NOT)**: Inverts all the bits.
- **`<<` (Left Shift)**: Shifts bits to the left (equivalent to multiplying by powers of two).
- **`>>` (Right Shift)**: Shifts bits to the right (equivalent to dividing by powers of two).
