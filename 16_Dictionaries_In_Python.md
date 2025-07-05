# Dictionaries In Python 📘


 A dictionary in Python is an unordered collection of items. Each item is stored as a pair, consisting of a key and a value. Keys must be unique and immutable (which means you can use types like strings, numbers, or tuples as keys), while values can be of any data type and can be duplicated.

---

## **1. Key Features of Dictionaries** 💡


Here are **five key features** of dictionaries in Python:

### 🌟**1.1. Unordered Collection** 
Dictionaries are unordered collections of key-value pairs. The items do not have a specific order, which means the insertion order is not guaranteed to be maintained in earlier versions of Python (before Python 3.7).

### 🌟**1.2. Mutable**
Dictionaries are mutable, which means you can change, add, or remove items after the dictionary is created.

### 🌟**1.3. Key-Value Pairs**
Dictionaries store data as **key-value pairs**. Each key must be unique, and it is associated with a specific value.

### 🌟**1.4. Keys Must Be Immutable**
The keys in a dictionary must be of an immutable data type, such as strings, numbers, or tuples, whereas the values can be of any data type and can even be mutable.

### 🌟**1.5. Fast Lookup**
Dictionaries provide fast lookups for data. Using the key, you can access the corresponding value in constant time, making dictionaries highly efficient for lookups.

---

## **2. Syntax of Dictionaries** 📚

The syntax for dictionaries involves enclosing key-value pairs in curly braces `{}`, where each key is followed by a colon `:`, and the value follows the colon.

### **Syntax:**
```python
my_dict = {
    'key1': 'value1',
    'key2': 'value2',
    'key3': 'value3'
}
```

---

## **3. Creating a Dictionary** 🛠️

There are multiple ways to create a dictionary in Python:

### ✨**3.1. Using Curly Braces**
```python
my_dict = {
    'name': 'Alice',
    'age': 30,
    'city': 'New York'
}
```

### ✨**3.2. Using the `dict()` Constructor**
```python
my_dict = dict(name='Alice', age=30, city='New York')
```

### ✨**3.3. Creating an Empty Dictionary**
```python
empty_dict = {}
```

---

## **4. Accessing Dictionary Elements** 🔍

You can access the values in a dictionary using the keys. If a key is not present, you will get a `KeyError`.

### 🔥**4.1. Accessing Using Brackets `[]`**
```python
my_dict = {'name': 'Alice', 'age': 30}
print(my_dict['name'])  # Output: Alice
```

### 🔥**4.2. Accessing Using the `get()` Method**
The `get()` method is safer because it returns `None` or a default value if the key is not found.
```python
print(my_dict.get('age'))        # Output: 30
print(my_dict.get('address'))    # Output: None
print(my_dict.get('address', 'Unknown'))  # Output: Unknown
```

---

## **5. Adding and Updating Dictionary Elements** 🔍

### **5.1. Adding New Key-Value Pairs**
You can add new key-value pairs by assigning a value to a new key.
```python
my_dict['country'] = 'USA'
print(my_dict)  # Output: {'name': 'Alice', 'age': 30, 'country': 'USA'}
```

### **5.2. Updating Existing Key-Value Pairs** 🔍
Assign a new value to an existing key.
```python
my_dict['age'] = 31
print(my_dict)  # Output: {'name': 'Alice', 'age': 31, 'country': 'USA'}
```

---

## **6. Removing Dictionary Elements** ⚠️

Python provides several methods to remove items from a dictionary:

### 🔥**6.1. Using `del` Statement**
Removes the specified key-value pair.
```python
del my_dict['country']
print(my_dict)  # Output: {'name': 'Alice', 'age': 31}
```

### 🔥**6.2. Using `pop()` Method**
Removes the key-value pair and returns the value.
```python
age = my_dict.pop('age')
print(age)       # Output: 31
print(my_dict)   # Output: {'name': 'Alice'}
```

### 🔥**6.3. Using `clear()` Method**
Removes all items from the dictionary.
```python
my_dict.clear()
print(my_dict)  # Output: {}
```

---

## **7. Dictionary Methods** ⚙️

Here are **8 useful dictionary methods**:

### 🏅**7.1. `keys()`**
Returns a view object that contains all the keys in the dictionary.
```python
my_dict = {'name': 'Alice', 'age': 30}
print(my_dict.keys())  # Output: dict_keys(['name', 'age'])
```

### 🏅**7.2. `values()`**
Returns a view object containing all the values in the dictionary.
```python
print(my_dict.values())  # Output: dict_values(['Alice', 30])
```

### 🏅**7.3. `items()`**
Returns a view object containing all the key-value pairs.
```python
print(my_dict.items())  # Output: dict_items([('name', 'Alice'), ('age', 30)])
```

### 🏅**7.4. `update()`**
Updates the dictionary with key-value pairs from another dictionary.
```python
my_dict.update({'city': 'New York'})
print(my_dict)  # Output: {'name': 'Alice', 'age': 30, 'city': 'New York'}
```

### 🏅**7.5. `pop()`**
Removes the specified key and returns the corresponding value.
```python
age = my_dict.pop('age')
print(age)  # Output: 30
```

### 🏅**7.6. `popitem()`**
Removes the last inserted key-value pair and returns it as a tuple.
```python
my_dict = {'name': 'Alice', 'age': 30, 'city': 'New York'}
item = my_dict.popitem()
print(item)  # Output: ('city', 'New York')
```

### 🏅**7.7. `copy()`**
Returns a shallow copy of the dictionary.
```python
new_dict = my_dict.copy()
```

### 🏅**7.8. `fromkeys()`**
Creates a new dictionary with specified keys and a common value.
```python
keys = ['name', 'age', 'city']
new_dict = dict.fromkeys(keys, 'Unknown')
print(new_dict)  # Output: {'name': 'Unknown', 'age': 'Unknown', 'city': 'Unknown'}
```

---

## **8. Dictionary Iteration** 💬

You can iterate through a dictionary's keys, values, or key-value pairs:

### **8.1. Iterating Through Keys**
```python
for key in my_dict:
    print(key)
```

### **8.2. Iterating Through Values**
```python
for value in my_dict.values():
    print(value)
```

### **8.3. Iterating Through Key-Value Pairs**
```python
for key, value in my_dict.items():
    print(f"{key}: {value}")
```

---

## **9. Dictionary Comprehension** 📝

Dictionary comprehension is a concise way to create dictionaries from iterables. It follows the pattern:

```python
{key_expression: value_expression for item in iterable}
```

### **Example:**
```python
squares = {x: x**2 for x in range(5)}
print(squares)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```

### **With Conditional Logic:** 💬
```python
even_squares = {x: x**2 for x in range(10) if x % 2 == 0}
print(even_squares)  # Output: {0: 0, 2: 4, 4: 16, 6: 36, 8: 64}
```

---

## **10. Nested Dictionaries** 📝

A dictionary can contain another dictionary as a value, allowing you to store complex data structures.

### **Example:**
```python
nested_dict = {
    'person1': {'name': 'Alice', 'age': 30},
    'person2': {'name': 'Bob', 'age': 25}
}

# Accessing nested dictionary elements
print(nested_dict['person1']['name'])  # Output: Alice
```

### **Modifying Nested Dictionary** 📝
```python
nested_dict['person2']['age'] = 26
print(nested_dict)  # {'person1': {'name': 'Alice', 'age': 30}, 'person2': {'name': 'Bob', 'age': 26}}
```

---

##  🏁 **Conclusion**

Dictionaries in Python are highly versatile and efficient for data management. We've covered their features, syntax, creation, and various operations like accessing, modifying, iterating, comprehension, and working with nested dictionaries.