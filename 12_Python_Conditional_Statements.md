# 🧩 Conditional Statements In Python :-

Let's explore **conditional statements** in Python, which allow you to execute different blocks of code based on specific conditions. The primary conditional statements in Python are the `if`, `elif`, and `else` statements.

---

## 🔹 **1. The `if` Statement**

The `if` statement evaluates a condition and executes a block of code if the condition is `True`.

### **Syntax**
```python
if condition:
    # Code block to execute if condition is True
```

### **Example**
```python
age = 18

if age >= 18:
    print("You are an adult.")
```
**Output:**
```
You are an adult.
```

**Explanation:**  
In this example, since the condition `age >= 18` evaluates to `True`, the code inside the `if` block is executed, printing the message.

---

## 🔹 **2. The `else` Statement**

The `else` statement can be added to execute a block of code when the `if` condition evaluates to `False`.

### **Syntax**
```python
if condition:
    # Code block if condition is True
else:
    # Code block if condition is False
```

### **Example**
```python
age = 16

if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```
**Output:**
```
You are a minor.
```

**Explanation:**  
Here, since `age` is `16`, the condition `age >= 18` evaluates to `False`, so the code inside the `else` block is executed.

---

## 🔹 **3. The `elif` Statement**

The `elif` (short for "else if") statement allows you to check multiple expressions for `True` and execute a block of code as soon as one of the conditions is `True`.

### **Syntax**
```python
if condition1:
    # Code block if condition1 is True
elif condition2:
    # Code block if condition2 is True
else:
    # Code block if both conditions are False
```

### **Example**
```python
age = 20

if age < 13:
    print("You are a child.")
elif age < 18:
    print("You are a teenager.")
else:
    print("You are an adult.")
```
**Output:**
```
You are an adult.
```

**Explanation:**  
In this case, the first condition (`age < 13`) is `False`, and the second condition (`age < 18`) is also `False`. Therefore, the code inside the `else` block is executed.

---

## 🔹 **4. Nested Conditional Statements**

You can also nest conditional statements inside other `if`, `elif`, or `else` statements.

### **Example**
```python
age = 22

if age >= 18:
    print("You are an adult.")
    if age >= 21:
        print("You can legally drink alcohol.")
else:
    print("You are a minor.")
```
**Output:**
```
You are an adult.
You can legally drink alcohol.
```

**Explanation:**  
Here, since `age` is `22`, the outer `if` statement evaluates to `True`, executing the first print statement. The inner `if` statement also evaluates to `True`, so the second print statement is executed.

---

## 🔹 **5. Using Logical Operators**

You can combine multiple conditions using logical operators like `and`, `or`, and `not`.

### **Example with `and` Operator**
```python
age = 20
has_permission = True

if age >= 18 and has_permission:
    print("You can enter the club.")
else:
    print("You cannot enter the club.")
```
**Output:**
```
You can enter the club.
```

**Explanation:**  
In this example, both conditions must be `True` for the code block to execute.

### **Example with `or` Operator**
```python
is_weekend = True
is_holiday = False

if is_weekend or is_holiday:
    print("You can sleep in!")
else:
    print("You have to wake up early.")
```
**Output:**
```
You can sleep in!
```

**Explanation:**  
Here, if either `is_weekend` or `is_holiday` is `True`, the code block executes.

---

## 🔹 **6. Ternary Operator (Conditional Expression)**

Python supports a shorthand way to write conditional statements using a ternary operator. It is a single-line expression that assigns a value based on a condition.

### **Syntax**
```python
variable = value_if_true if condition else value_if_false
```

### **Example**
```python
age = 15
status = "Adult" if age >= 18 else "Minor"
print(status)
```
**Output:**
```
Minor
```

**Explanation:**  
In this case, `status` is assigned `"Minor"` since the condition evaluates to `False`.

---

## ✅ **Conclusion**

Conditional statements in Python allow you to control the flow of your program based on conditions. Mastering these statements will enable you to write more dynamic and responsive code.


