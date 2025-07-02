

# 🔁 **Loops In Python** :-

Explore **loops in Python**, essential for executing a block of code multiple times based on specific conditions. Python primarily uses two types of loops: **for loops** and **while loops**.

---

## **1. For Loops** 🔄

The `for` loop is used to iterate over a sequence (like a list, tuple, string, or range). It executes a block of code for each item in the sequence.

### **Syntax**
```python
for variable in sequence:
    # Code block to be executed
```

### **Example: Using `for` with a List** 🍎
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```
**Output:**
```
apple
banana
cherry
```

### **Example: Using `for` with `range()`** 🔢
The `range()` function generates a sequence of numbers, which can be helpful for looping a specific number of times.

```python
for i in range(5):
    print(i)
```
**Output:**
```
0
1
2
3
4
```

### **Using `for` with Strings** ✍️
You can also iterate over the characters in a string.

```python
word = "Hello"
for letter in word:
    print(letter)
```
**Output:**
```
H
e
l
l
o
```

---

## **2. While Loops** 🔂

A `while` loop repeatedly executes a block of code as long as a specified condition is `True`.

### **Syntax**
```python
while condition:
    # Code block to be executed
```

### **Example: Basic While Loop** 🧮
```python
count = 0
while count < 5:
    print(count)
    count += 1
```
**Output:**
```
0
1
2
3
4
```

### **Example: Infinite Loop** ♾️
A `while` loop can potentially create an infinite loop if the condition never becomes `False`.

```python
count = 0
while True:
    print(count)
    count += 1
    if count >= 5:
        break  # Break out of the loop
```
**Output:**
```
0
1
2
3
4
```

---

## **3. Loop Control Statements** 🚦

Python provides several control statements to alter the flow of loops:

### **a. `break` Statement** ⛔
The `break` statement exits a loop prematurely when a specific condition is met.

#### Example:
```python
for i in range(10):
    if i == 5:
        break  # Exit the loop when i is 5
    print(i)
```
**Output:**
```
0
1
2
3
4
```

### **b. `continue` Statement** ⏭️
The `continue` statement skips the rest of the code inside the loop for the current iteration and moves to the next iteration.

#### Example:
```python
for i in range(5):
    if i == 2:
        continue  # Skip the iteration when i is 2
    print(i)
```
**Output:**
```
0
1
3
4
```

### **c. `pass` Statement** 📜
The `pass` statement does nothing and serves as a placeholder when a statement is required syntactically but no action is needed.

#### Example:
```python
for i in range(5):
    if i == 2:
        pass  # Does nothing when i is 2
    print(i)
```
**Output:**
```
0
1
2
3
4
```

---

## **4. Nested Loops** 🔄🔄

You can place one loop inside another. The inner loop runs completely for each iteration of the outer loop.

### **Example: Nested For Loop** 📊
```python
for i in range(3):       # Outer loop
    for j in range(2):   # Inner loop
        print(f"i={i}, j={j}")
```
**Output:**
```
i=0, j=0
i=0, j=1
i=1, j=0
i=1, j=1
i=2, j=0
i=2, j=1
```

---

## **5. Looping Techniques** 🔍

### **a. Looping through Dictionaries** 📖
You can loop through the keys and values of a dictionary using `.items()`.

```python
my_dict = {"a": 1, "b": 2, "c": 3}
for key, value in my_dict.items():
    print(f"Key: {key}, Value: {value}")
```
**Output:**
```
Key: a, Value: 1
Key: b, Value: 2
Key: c, Value: 3
```

### **b. Looping with `enumerate()`** 🏷️
The `enumerate()` function adds a counter to the loop, providing both index and value.

```python
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(f"Index: {index}, Fruit: {fruit}")
```
**Output:**
```
Index: 0, Fruit: apple
Index: 1, Fruit: banana
Index: 2, Fruit: cherry
```

---

## **6. do-While Loops in Python** 🔁

Python does not have a built-in `do-while` loop, but you can simulate it using a `while` loop and a `break` statement.

### **Simulating a Do-While Loop** 📝
In a `do-while` loop, the code block executes at least once before checking the condition for continuation.

### **Example**
```python
count = 0

while True:  # Start with an infinite loop
    print(count)
    count += 1
    if count >= 5:  # Condition to stop the loop
        break  # Break out of the loop when count is 5
```

**Output:**
```
0
1
2
3
4
```

---

## **Conclusion** ✅

Loops are powerful tools in Python that allow you to automate repetitive tasks efficiently. Understanding `for` and `while` loops, along with control statements and nested loops, will greatly enhance your programming skills.