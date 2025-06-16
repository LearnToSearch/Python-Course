# 📥 Basic Input And Output In Python :-

### 1. **Input in Python** 📝
Python uses the `input()` function to take user input. This function reads the input as a string, so if you need another type (like an integer or float), you have to convert it explicitly.

#### Basic Syntax:
```python
variable = input(prompt)
```

#### Examples:
```python
# Take a simple input
name = input("Enter your name: ")
print("Hello,", name)

# Take an integer input
age = int(input("Enter your age: "))
print("You are", age, "years old.")

# Take a float input
height = float(input("Enter your height in meters: "))
print("Your height is", height, "meters.")
```

#### Converting Input:
Since `input()` always returns a string, you need to convert it to an integer, float, etc., depending on your use case:

```python
number = int(input("Enter a number: "))   # Converts input to integer
pi = float(input("Enter a value for pi: "))  # Converts input to float
```

### 2. **Examples of Basic Input and Output** 📊
Here’s a simple program that takes the user's name, age, and height, and then prints a message:

```python
# Input
name = input("What is your name? ")
age = int(input("How old are you? "))
height = float(input("How tall are you (in meters)? "))

# Output using f-strings
print(f"Hello {name}, you are {age} years old and {height} meters tall.")
```

### 3. **Output in Python** 📤
Python uses the `print()` function to display output to the console. You can print strings, numbers, variables, and even multiple items at once.

#### Basic Syntax:
```python
print(object, ...)
```

#### Examples:
```python
# Print a string
print("Hello, World!")

# Print a number
print(42)

# Print a variable
name = "Alice"
print(name)

# Print multiple values
age = 25
print("Name:", name, "Age:", age)
```

#### Output Format:
You can also format your output using **f-strings** (formatted string literals) or the `.format()` method:

##### Using f-strings (Python 3.6+):
```python
name = "Alice"
age = 25
print(f"Name: {name}, Age: {age}")
```

##### Using `.format()`:
```python
print("Name: {}, Age: {}".format(name, age))
```

---

### 📚 Summary:
- **Output**: Use `print()` to display information.
- **Input**: Use `input()` to capture user input, and convert it to the required type if needed.
```

