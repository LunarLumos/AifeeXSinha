# 🐍 DAY 2 – Control Flow & Functions

---

## **1. Comparison Operators**

Comparison operators are used to **compare two values**. They always return a **Boolean value** (`True` or `False`).

| Operator | Meaning               | Example   | Result |
| -------- | --------------------- | --------- | ------ |
| `==`     | Equal to              | `5 == 5`  | True   |
| `!=`     | Not equal             | `5 != 3`  | True   |
| `<`      | Less than             | `3 < 5`   | True   |
| `>`      | Greater than          | `5 > 3`   | True   |
| `<=`     | Less than or equal    | `5 <= 5`  | True   |
| `>=`     | Greater than or equal | `7 >= 10` | False  |

### Example:

```python
x = 10
y = 5
print(x == y)  # False
print(x != y)  # True
print(x > y)   # True
```

---

## **2. Logical Operators**

Used to **combine multiple conditions**.

| Operator | Meaning                      | Example           | Result                |
| -------- | ---------------------------- | ----------------- | --------------------- |
| `and`    | Both conditions must be True | `x > 0 and y > 0` | True if both are True |
| `or`     | At least one condition True  | `x > 0 or y < 0`  | True if any is True   |
| `not`    | Negates the condition        | `not(x > y)`      | True if x ≤ y         |

### Example:

```python
x = 10
y = 5
print(x > 0 and y > 0)   # True
print(x < 0 or y > 0)    # True
print(not(x == y))       # True
```

---

## **3. Conditional Statements**

Python executes **code based on conditions** using `if`, `elif`, and `else`.

### Syntax:

```python
if condition:
    # block of code
elif another_condition:
    # block of code
else:
    # block of code
```

### Example:

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
```

---

### **3.1 Nesting Conditions**

You can put **if statements inside another if**.

```python
num = int(input("Enter a number: "))

if num > 0:
    if num % 2 == 0:
        print("Positive even number")
    else:
        print("Positive odd number")
else:
    print("Non-positive number")
```

---

## **4. Functions**

Functions allow you to **reuse code** and **organize logic**.

### **4.1 Defining a Function**

```python
def greet():
    print("Hello, World!")
```

Call it:

```python
greet()
```

---

### **4.2 Parameters vs Arguments**

* **Parameters** → placeholders in function definition
* **Arguments** → actual values passed to the function

```python
def greet(name):  # 'name' is parameter
    print(f"Hello, {name}!")

greet("Aifee")  # "Aifee" is argument
```

---

### **4.3 Return Values**

* Functions can **return a value** using `return`.

```python
def add(a, b):
    return a + b

result = add(5, 7)
print(result)  # 12
```

---

### **4.4 Scope (Local vs Global Variables)**

* **Local variable** → Exists inside a function
* **Global variable** → Exists outside all functions

```python
x = 10  # global

def func():
    y = 5  # local
    print("Inside function:", x, y)

func()
print("Outside function:", x)
# print(y)  # ERROR: y is not defined
```

* To modify a global variable inside a function:

```python
x = 10

def update():
    global x
    x += 5

update()
print(x)  # 15
```

---

## **5. Basic Error Handling**

Python can **catch errors** using `try`, `except`, and optionally `finally`.

### **Syntax**

```python
try:
    # code that might fail
except SomeError:
    # code to handle the error
finally:
    # code that always runs (optional)
```

### **Example 1: ValueError**

```python
try:
    num = int(input("Enter a number: "))
    print("You entered:", num)
except ValueError:
    print("That was not a valid number!")
```

### **Example 2: ZeroDivisionError**

```python
try:
    a = 10
    b = int(input("Enter a divisor: "))
    print(a / b)
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### **Example 3: Finally**

```python
try:
    f = open("file.txt")
except FileNotFoundError:
    print("File not found!")
finally:
    print("Execution finished.")
```

---

## 🎯 **Day 2 Goal**

By the end of Day 2, you should be able to:
✅ Make **decisions in code** using `if`, `elif`, `else`
✅ Combine multiple conditions with `and`, `or`, `not`
✅ Write **reusable functions** with parameters and return values
✅ Understand **scope of variables**
✅ Handle **basic runtime errors** safely

---

## 💻 **Practice Exercises**

### **Exercise 1 – Odd or Even**

Ask the user for a number and print if it’s odd or even.

### **Exercise 2 – Grade Checker**

Ask the user for a score (0–100) and print grade:

* 90–100 → A
* 80–89 → B
* 70–79 → C
* 60–69 → D
* <60 → F

### **Exercise 3 – Function Calculator**

Write a function that takes two numbers and prints:

* Sum
* Difference
* Product
* Division (handle division by zero)

### **Exercise 4 – Nested Conditions**

Ask for age and gender, then print:

* "Adult Male"
* "Adult Female"
* "Teen Male"
* "Teen Female"
* "Child"

### **Exercise 5 – Error Handling**

Write a program that asks for a number and divides 100 by that number.
Handle both `ValueError` and `ZeroDivisionError`.

---
