# 🔧 Functions in Python :-

---

## 💡 **1. What is a Function?**

A function is a reusable block of code that performs a specific task. Functions can take inputs (arguments), perform operations, and return outputs.

---

## 🛠️ **2. Defining a Function**

To define a function in Python, use the `def` keyword followed by the function name and parentheses. The code block within the function is indented.

### 📝 **Syntax**
```python
def function_name(parameters):
    # Code block
    return value  # Optional
```

### 🖥️ **Example: Basic Function Definition**
```python
def greet():
    print("Hello, World!")

greet()  # Calling the function
```
**📌 Output:**
```
Hello, World!
```

**🔍 Explanation:**  
Here, `greet` is a function that prints a greeting. The function is called using its name followed by parentheses.

---

## 🎛️ **3. Function Parameters and Arguments**

Functions can accept inputs, known as **parameters**. When you call a function, the values you pass to it are called **arguments**.

### ⚙️ **Example: Function with Parameters**
```python
def add(a, b):
    return a + b

result = add(5, 3)  # Calling the function with arguments
print(result)  # Output: 8
```
**📌 Output:**
```
8
```

**🔍 Explanation:**  
In this example, the function `add` takes two parameters, `a` and `b`, and returns their sum. The function is called with the arguments `5` and `3`, and the result is printed.

---

## ⚖️ **4. Default Parameters**

You can define default values for parameters. If no argument is provided for a default parameter, the default value is used.

### ⚙️ **Example: Function with Default Parameters**
```python
def greet(name="Guest"):
    print(f"Hello, {name}!")

greet()            # Uses default value
greet("Alice")     # Overrides default value
```
**📌 Output:**
```
Hello, Guest!
Hello, Alice!
```

**🔍 Explanation:**  
The `greet` function has a default parameter `name` set to `"Guest"`. If no argument is passed, it uses the default. If an argument is provided, it uses that value instead.

---

## 🔄 **5. Return Statement**

The `return` statement is used to exit a function and send a value back to the caller.

### 💬 **Example: Using Return Statement**
```python
def multiply(a, b):
    return a * b

product = multiply(4, 5)
print(product)  # Output: 20
```
**📌 Output:**
```
20
```

**🔍 Explanation:**  
The `multiply` function returns the product of `a` and `b`. The returned value is stored in the variable `product` and printed.

---

## 🔒 **6. Variable Scope**

Variables defined inside a function are local to that function and cannot be accessed outside it. This is called **scope**.

### 🌐 **Example: Variable Scope**
```python
def my_function():
    x = 10  # Local variable
    print("Inside the function:", x)

my_function()
# print(x)  # This will raise an error because x is not accessible here
```
**📌 Output:**
```
Inside the function: 10
```

**🔍 Explanation:**  
The variable `x` is defined inside `my_function`, making it local to that function. Trying to access `x` outside the function raises a `NameError`.

---

## 📜 **7. Function Docstrings**

You can add documentation to your functions using docstrings. A docstring is a string literal that describes what the function does.

### 📖 **Example: Function Docstring**
```python
def subtract(a, b):
    """Subtracts b from a and returns the result."""
    return a - b

print(subtract.__doc__)  # Output: Subtracts b from a and returns the result.
```
**📌 Output:**
```
Subtracts b from a and returns the result.
```

**🔍 Explanation:**  
The docstring provides information about what the `subtract` function does. You can access it using the `__doc__` attribute.

---

## ⚡ **8. Lambda Functions**

Python also supports anonymous functions, known as **lambda functions**. These are defined using the `lambda` keyword.

### ⚙️ **Example: Lambda Function**
```python
add = lambda x, y: x + y
result = add(3, 5)
print(result)  # Output: 8
```
**📌 Output:**
```
8
```

**🔍 Explanation:**  
Here, `add` is a lambda function that takes two arguments and returns their sum. Lambda functions are often used for short, throwaway functions.

---

## 🌀 **9. Higher-Order Functions**

Functions in Python can take other functions as arguments or return functions. This is known as a higher-order function.

### 🔗 **Example: Higher-Order Function**
```python
def apply_function(func, value):
    return func(value)

result = apply_function(lambda x: x ** 2, 5)  # Passing a lambda function
print(result)  # Output: 25
```
**📌 Output:**
```
25
```

**🔍 Explanation:**  
The `apply_function` takes a function (`func`) and a value (`value`) as arguments. In this case, a lambda function that squares the number is passed, and the result is printed.

---

## 🔁 **10. Recursion**

A function can call itself, which is known as **recursion**. This is often used for problems that can be broken down into smaller, similar subproblems.

### 💫 **Example: Recursive Function**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```
**📌 Output:**
```
120
```

**🔍 Explanation:**  
The `factorial` function calculates the factorial of `n` by calling itself with a smaller value (`n - 1`) until it reaches the base case (`n == 0`).

---

## 📈 **Conclusion**

Functions in Python are powerful tools for organizing code and enhancing reusability. Understanding how to define, call, and utilize functions is fundamental to effective programming. 


