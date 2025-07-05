# 📂 File Handling in Python :-

In this guide, we’ll explore **file handling** in Python, covering essential topics. File handling is critical for reading from and writing to files, managing data storage, and performing various file operations.

---

## **1. 📄 Opening Files in Various Modes**

When working with files, you need to specify the mode in which you want to open the file. Here are the common file modes:

### **1.1. 🔍 Modes Explained**

- **`'r'`**: 📝 Read mode. Opens the file for reading; the file must exist. If the file does not exist, an error will be raised.
- **`'w'`**: ✍️ Write mode. Opens the file for writing; creates the file if it does not exist or truncates the file if it already exists.
- **`'a'`**: ➕ Append mode. Opens the file for writing; creates the file if it does not exist. Data is written at the end of the file.
- **`'rb'`**: 📷 Read binary mode. Opens the file for reading in binary format. Useful for files like images or audio.
- **`'wb'`**: 🖋️ Write binary mode. Opens the file for writing in binary format. Creates the file if it does not exist or truncates it if it does.
- **`'r+'`**: 🔄 Read and write mode. Opens the file for both reading and writing. The file must exist; it will not be created if it doesn't.
- **`'w+'`**: ✏️ Write and read mode. Opens the file for reading and writing. Creates the file if it does not exist or truncates it if it does.
- **`'a+'`**: 🔄 Append and read mode. Opens the file for both appending and reading. Creates the file if it does not exist. Data is added at the end of the file.

### **1.2. 📝 Examples of Opening Files**

#### 📖 Example of Opening a File in Read Mode
```python
# Opening a file in read mode
try:
    file = open('example.txt', 'r')
    print(file.read())
finally:
    file.close()
```

#### ✍️ Example of Opening a File in Write Mode
```python
# Opening a file in write mode
with open('example.txt', 'w') as file:
    file.write("Hello, World!\n")
```

#### ➕ Example of Opening a File in Append Mode
```python
# Opening a file in append mode
with open('example.txt', 'a') as file:
    file.write("Appending a new line.\n")
```

#### 📷 Example of Opening a File in Binary Read Mode
```python
# Opening a binary file for reading
with open('image.png', 'rb') as file:
    binary_data = file.read()
    print("Read binary data:", binary_data[:10])  # Print first 10 bytes
```

---

## **2. 📑 Reading from and Writing to Files**

### **2.1. 📖 Reading from Files**

Python provides several methods for reading from files:

- **`read(size)`**: Reads a specified number of bytes. If no size is specified, reads the entire file.
- **`readline()`**: Reads a single line from the file.
- **`readlines()`**: Reads all lines and returns a list.

#### Example of 📖 Reading from a File
```python
with open('example.txt', 'r') as file:
    content = file.read()  # Read entire file
    print("File Content:", content)

# Read line by line
with open('example.txt', 'r') as file:
    for line in file:
        print("Line:", line.strip())
```

### **2.2. ✏️ Writing to Files**

To write data to a file, you can use the `write()` method.

#### Example of ✏️ Writing to a File
```python
with open('example.txt', 'w') as file:
    file.write("Writing this line to the file.\n")
```

### **2.3. 🖊️ Writing Multiple Lines**

You can use `writelines()` to write a list of strings to a file.

#### Example of 🖊️ Writing Multiple Lines
```python
lines = ["First line\n", "Second line\n", "Third line\n"]
with open('example.txt', 'w') as file:
    file.writelines(lines)
```

---

## **3. 📍 File Pointer**

A file pointer keeps track of the current position in a file. When you read or write to a file, the file pointer moves accordingly.

### **3.1. 📌 Using the `tell()` Method**

The `tell()` method returns the current position of the file pointer.

#### Example of Using 📌 `tell()`
```python
with open('example.txt', 'r') as file:
    print("Current position:", file.tell())  # Output: 0
    file.read(5)  # Read first 5 characters
    print("Current position after reading:", file.tell())  # Output: 5
```

### **3.2. ⏩ Using the `seek(offset, whence)` Method**

The `seek()` method changes the file pointer's position. The `offset` indicates how many bytes to move, and `whence` determines the reference point for the offset.

- **`whence = 0`**: Start of the file.
- **`whence = 1`**: Current position.
- **`whence = 2`**: End of the file.

#### Example of Using ⏩ `seek()`
```python
with open('example.txt', 'r') as file:
    file.read(5)  # Read first 5 characters
    print("Current position:", file.tell())  # Output: 5
    file.seek(0)  # Move back to the beginning
    print("Position after seek:", file.tell())  # Output: 0
```

---

## **4. 🚨 Handling File Exceptions**

File operations can lead to exceptions, such as trying to read a non-existent file or writing to a read-only file. To handle these exceptions, use `try-except` blocks.

### Example of 🚨 Handling File Exceptions
```python
try:
    with open('non_existent_file.txt', 'r') as file:
        content = file.read()
except FileNotFoundError:
    print("Error: The file does not exist.")
except IOError:
    print("Error: Could not read the file.")
```

---

## **5. ✅ Using `with` for Better File Handling**

Using the `with` statement ensures that files are properly closed after their suite finishes executing. This is a best practice as it reduces the risk of leaving files open unintentionally.

### Example of Using ✅ `with`
```python
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
# No need to call file.close(), it's automatically handled.
```

---

## **6. 🏁 Conclusion**

File handling in Python is straightforward and provides various functionalities to read, write, and manage files. Understanding file modes, reading/writing methods, the concept of file pointers, exception handling, and using the `with` statement can greatly enhance your ability to work with files effectively.