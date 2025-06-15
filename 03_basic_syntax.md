# 🐍 Python Basics :-

### 1. **Hello World in Python** 🌍

A "Hello, World!" program is often the first program written when learning a new language. It's simple and demonstrates how to print text to the screen.

In Python, this can be done using the `print()` function:

```python
print("Hello, World!")
```

- The `print()` function is a built-in function in Python that outputs data to the console.
- The text inside the parentheses `"Hello, World!"` is a string (sequence of characters) enclosed in double quotes (`""`). You can also use single quotes (`'Hello, World!'`).

When executed, the program will display:

```
Hello, World!
```

---

### 2. **The `print()` Statement** 🖨️

The `print()` function in Python outputs whatever is passed to it to the console. It can take various types of arguments, including strings, numbers, and even complex data types like lists and dictionaries.

#### Basic Usage

```python
# Printing a string
print("Hello, Python!")

# Printing numbers
print(10)
print(3.14)

# Printing multiple values
print("My age is", 25)

# Printing variables
name = "Alice"
age = 30
print("Name:", name, "Age:", age)
```

#### Important Features of `print()`:
- By default, `print()` ends with a newline character (`\n`), meaning that each call to `print()` starts on a new line.
  
    ```python
    print("Hello")
    print("World")
    ```
    Output:
    ```
    Hello
    World
    ```

- To change the ending, use the `end` parameter:

    ```python
    print("Hello", end=" ")
    print("World")
    ```
    Output:
    ```
    Hello World
    ```

- You can also change the separator between multiple arguments using the `sep` parameter:

    ```python
    print("Hello", "World", sep="---")
    ```
    Output:
    ```
    Hello---World
    ```

#### Printing Data Types

The `print()` function automatically converts different data types to strings for display. For example:

```python
a = 10
b = 3.14
c = [1, 2, 3]
print(a, b, c)
```
Output:
```
10 3.14 [1, 2, 3]
```

---

### 3. **Python Comments 💬**

Comments are lines in the code that are not executed by the Python interpreter. They are used to explain the code, making it more readable and easier to understand. Comments can also be used to temporarily disable parts of the code during debugging.

#### Types of Comments:

1. **Single-line Comments**: These are created using the `#` symbol. Anything following the `#` on that line is ignored by Python.

    ```python
    # This is a single-line comment
    print("This will run")  # This is also a comment
    ```

    Output:
    ```
    This will run
    ```

2. **Multi-line Comments (Docstrings)**: Although Python doesn’t have a formal syntax for multi-line comments, you can use triple quotes (`'''` or `"""`) to create them. Technically, these are called docstrings and are primarily used for documenting functions, classes, or modules.

    ```python
    """
    This is a multi-line comment.
    It can span multiple lines.
    """
    print("This will run too")
    ```

    Output:
    ```
    This will run too
    ```

3. **Use Case**: Docstrings are generally used for documentation purposes, whereas single-line comments are used for explaining specific parts of code.

    ```python
    def add(a, b):
        """
        This function adds two numbers.
        Parameters:
        a - First number
        b - Second number
        Returns the sum of a and b.
        """
        return a + b
    ```

---

### 4. **Python Indentation ⏳**

In most programming languages, code blocks are defined using curly braces `{}` or keywords. However, Python uses **indentation** (whitespace) to define blocks of code.

#### Importance of Indentation:

Indentation in Python is **mandatory** and is used to define the hierarchy and structure of the code. All lines of code within the same block must be indented with the same number of spaces (commonly 4 spaces or a tab).

**Example of Correct Indentation**:
```python
if 5 > 2:
    print("Five is greater than two")  # This is indented with 4 spaces
    print("This is part of the if block")  # Still part of the if block
print("This is outside the if block")  # This is not indented, hence outside the if block
```

**Example of Incorrect Indentation**:
```python
if 5 > 2:
print("This will cause an error")  # Incorrect indentation (should be indented)
```
This will result in an **IndentationError** because Python expects indented code following the `if` statement.

#### Indentation and Control Flow:

Blocks of code following `if`, `for`, `while`, and function definitions are indented. For example:

**For loops**:

```python
for i in range(5):
    print(i)  # This is part of the loop, indented by 4 spaces
print("Loop ended")  # This is outside the loop
```

**Functions**:

```python
def greet():
    print("Hello")  # This is part of the function block
    print("World")  # Still inside the function block
```

#### Best Practices for Indentation:
- Use **4 spaces** for each level of indentation. Most code editors, like VS Code or PyCharm, automatically insert 4 spaces when you press the Tab key.
- Be consistent with your indentation. Mixing spaces and tabs can lead to errors, so stick to one type (spaces are preferred).
- Python’s `IndentationError` will help you quickly identify if there’s a problem with your indentation.

---

### Summary 📝
- **Hello World**: The simplest Python program, demonstrating the `print()` function.
- **Print Statement**: Outputs text or values to the console, with optional parameters like `end` and `sep` to customize the output.
- **Comments**: Used to explain code, with single-line (`#`) and multi-line (`''' '''` or `""" """`) options.
- **Indentation**: Python uses indentation to define blocks of code. Consistent indentation is crucial to avoid errors.

By following these principles, Python code becomes more readable, clean, and easy to maintain. Happy coding! 🎉
```

