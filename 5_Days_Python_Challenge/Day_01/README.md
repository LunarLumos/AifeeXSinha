# 🐍 **DAY 1 – Python Fundamentals**

---

## **1. What is Python?**

### 📘 Definition:

Python is a **high-level**, **interpreted**, **general-purpose** programming language designed for simplicity and readability.
It was created by **Guido van Rossum** and released in **1991**.

### 💪 Key Features:

| Feature                 | Description                                          |
| ----------------------- | ---------------------------------------------------- |
| **Readable Syntax**     | Code looks like English. Easy to write & understand. |
| **Interpreted**         | No need to compile — Python runs line by line.       |
| **Cross-Platform**      | Works on Windows, macOS, and Linux.                  |
| **Dynamic Typing**      | No need to declare data types manually.              |
| **Extensive Libraries** | Built-in modules + thousands of external packages.   |

### 💡 Common Use Cases:

* **Data Science** (NumPy, Pandas, Matplotlib)
* **Machine Learning & AI** (TensorFlow, PyTorch)
* **Web Development** (Flask, Django)
* **Automation / Scripting**
* **Cybersecurity / Pen Testing** (Scapy, Pwntools)
* **Game Development** (Pygame)

---

## **2. Installing Python**

If you’re using **Google Colab**, **Replit**, or **Jupyter**, skip this.

### 🧩 Local Installation:

1. Go to [https://www.python.org/downloads](https://www.python.org/downloads)
2. Download and install Python (check **“Add Python to PATH”** box).
3. Verify installation:

   ```bash
   python --version
   ```

   or

   ```bash
   python3 --version
   ```

### 🧠 Run Python Code:

You can run Python code in:

* **VS Code**, **Thonny**, **PyCharm**, or terminal using:

  ```bash
  python filename.py
  ```

---

## **3. Hello, World!**

The first program in any language:

```python
print("Hello, World!")
```

### 🧩 Explanation:

* `print()` → built-in function to display output on screen.
* `"Hello, World!"` → string (text enclosed in quotes).

🖥️ Output:

```
Hello, World!
```

---

## **4. Variables and Assignment**

A **variable** is a container that stores data.

```python
name = "Aifee"
age = 20
height = 5.9
is_student = True
```

### 🧠 Rules:

* Must start with a letter or underscore (`_`)
* Can’t start with a number
* Case sensitive (`Age` ≠ `age`)
* Use underscores instead of spaces (`full_name`, not `full name`)

### 🧩 Example:

```python
x = 10
y = 20
sum = x + y
print(sum)
```

🖥️ Output:

```
30
```

---

## **5. Data Types**

| Type    | Example      | Description     |
| ------- | ------------ | --------------- |
| `int`   | 5, -10, 2000 | Whole numbers   |
| `float` | 3.14, -2.5   | Decimal numbers |
| `str`   | "Hello"      | Text (string)   |
| `bool`  | True, False  | Logical values  |

### Example:

```python
a = 12
b = 4.5
c = "Python"
d = True

print(type(a))
print(type(b))
print(type(c))
print(type(d))
```

🖥️ Output:

```
<class 'int'>
<class 'float'>
<class 'str'>
<class 'bool'>
```

---

## **6. Type Conversion**

Convert between data types using:

* `int()`
* `float()`
* `str()`
* `bool()`

### Example:

```python
x = "100"
y = int(x)
z = float(y)
s = str(z)
b = bool(1)

print(x, y, z, s, b)
```

🖥️ Output:

```
100 100 100.0 100.0 True
```

---

## **7. Taking Input**

Input always returns a **string**, so convert when needed.

### Example 1:

```python
name = input("Enter your name: ")
print("Hello,", name)
```

### Example 2 (with type conversion):

```python
age = int(input("Enter your age: "))
print(f"You are {age} years old.")
```

### Example 3:

```python
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
print("Sum =", num1 + num2)
```

---

## **8. String Formatting**

### 1️⃣ **f-strings (modern & preferred)**

```python
name = "Aifee"
age = 21
print(f"My name is {name} and I am {age} years old.")
```

### 2️⃣ **.format() method**

```python
print("My name is {} and I am {} years old.".format(name, age))
```

### 3️⃣ **Old-style (%) formatting**

```python
print("My name is %s and I am %d years old." % (name, age))
```

🧠 **Why formatting matters:**
It helps mix variables and text cleanly in output.

---

## **9. Comments**

Used to explain code or disable lines.

### Example:

```python
# This is a single-line comment

'''
This is
a multi-line comment
'''

"""
This also
works the same way
"""
```

🧩 Tip: Comments don’t affect code execution.

---

## **10. Useful Built-in Functions**

| Function  | Description           | Example            | Output          |
| --------- | --------------------- | ------------------ | --------------- |
| `type()`  | Check data type       | `type(10)`         | `<class 'int'>` |
| `len()`   | Length of string/list | `len("Python")`    | `6`             |
| `round()` | Round decimals        | `round(3.1416, 2)` | `3.14`          |
| `abs()`   | Absolute value        | `abs(-5)`          | `5`             |

### Example:

```python
x = -12.67
print(type(x))
print(abs(x))
print(round(x))
print(len("Python"))
```

🖥️ Output:

```
<class 'float'>
12.67
-13
6
```

---

## 🎯 **Goal Recap**

By end of Day 1, you should be able to:

✅ Understand Python’s core concepts and uses

✅ Write and run Python scripts

✅ Handle variables and data types

✅ Take user input and display formatted output

✅ Use built-in functions and comments

---

## 💻 **Mini Practice Exercises**

### 🧮 Exercise 1: Greeting Program

Write a program that asks for your name and age, then prints:

```
Hello Aifee, you are 21 years old!
```

---

### 🧮 Exercise 2: Calculator

Ask user for two numbers. Display:

* Sum
* Difference
* Product
* Quotient (division)

Example output:

```
Enter first number: 10
Enter second number: 5
Sum = 15
Difference = 5
Product = 50
Quotient = 2.0
```

---

### 🌡️ Exercise 3: Temperature Converter

Convert Celsius to Fahrenheit
Formula: `F = (C * 9/5) + 32`

```python
celsius = float(input("Enter temperature in Celsius: "))
fahrenheit = (celsius * 9/5) + 32
print(f"{celsius}°C = {fahrenheit}°F")
```

---

### 📏 Exercise 4: String Length

Ask user for a word and print how many letters it has.

```python
word = input("Enter a word: ")
print(f"'{word}' has {len(word)} letters.")
```

---

### 🧠 Exercise 5: Rounding and Absolute Value

```python
num = float(input("Enter a decimal number: "))
print("Absolute value:", abs(num))
print("Rounded value:", round(num, 2))
```

---
