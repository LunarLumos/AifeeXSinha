---

# 🐍 **DAY 4 – Data Structures & File I/O**

---

## 🧠 What You’ll Learn Today

You’ll learn about:

✅ Tuples (like lists but cannot change)

✅ Sets (no duplicates)

✅ Dictionaries (key–value storage)

✅ Reading and writing files

✅ Simple Python modules (`math`, `random`, `datetime`)

---

## 🟢 1. **Tuples**

### 📘 What is a Tuple?

A **tuple** is a collection (like a list), but **you cannot change it** after creating it.
We say it is **immutable** (cannot be modified).

---

### 🧩 Example:

```python
fruits = ("apple", "banana", "cherry")
print(fruits)
```

Output:

```
('apple', 'banana', 'cherry')
```

---

### 🎯 Accessing Elements:

You can get items using index numbers (like lists):

```python
print(fruits[0])  # apple
print(fruits[2])  # cherry
```

---

### ⚠️ You Can’t Change Tuples:

```python
fruits[1] = "orange"   # ❌ Error
```

---

### ✅ Why Use Tuples?

* They are **faster** than lists.
* Good for **fixed data** (like coordinates or dates).
* Example:

  ```python
  position = (10, 20)
  date = (2025, 10, 24)
  ```

---

### 🔄 Tuple Unpacking:

```python
person = ("Aifee", 20, "Student")
name, age, role = person
print(name)
print(age)
print(role)
```

Output:

```
Aifee
20
Student
```

---

## 🟡 2. **Sets**

### 📘 What is a Set?

A **set** is a collection of **unique** items.
That means **no duplicates** are allowed.

---

### 🧩 Example:

```python
numbers = {1, 2, 3, 3, 4, 4, 5}
print(numbers)
```

Output:

```
{1, 2, 3, 4, 5}   # duplicates are removed
```

---

### 🧰 Common Set Methods

| Method      | Description      | Example             |
| ----------- | ---------------- | ------------------- |
| `.add()`    | Add item         | `numbers.add(6)`    |
| `.remove()` | Remove item      | `numbers.remove(3)` |
| `.clear()`  | Remove all items | `numbers.clear()`   |

---

### 🔄 Set Operations:

```python
a = {1, 2, 3}
b = {3, 4, 5}

print(a.union(b))         # {1, 2, 3, 4, 5}
print(a.intersection(b))  # {3}
print(a.difference(b))    # {1, 2}
```

---

### 🎯 When to Use Sets?

* When you want to **remove duplicates**
* When you want to **compare data quickly**
* When order doesn’t matter

---

## 🔵 3. **Dictionaries**

### 📘 What is a Dictionary?

A dictionary is like a **real-life dictionary**:
Each word (key) has a meaning (value).

---

### 🧩 Example:

```python
student = {
    "name": "Aifee",
    "age": 20,
    "grade": "A"
}
```

---

### 🔍 Accessing Data:

```python
print(student["name"])   # Aifee
print(student["age"])    # 20
```

---

### ✏️ Adding / Changing Data:

```python
student["course"] = "Python"
student["age"] = 21
print(student)
```

---

### ❌ Deleting Data:

```python
del student["grade"]
print(student)
```

---

### 🔁 Looping through Dictionary:

```python
for key, value in student.items():
    print(key, ":", value)
```

Output:

```
name : Aifee
age : 21
course : Python
```

---

### 🧠 Nested Dictionary (Dictionary inside Dictionary)

```python
students = {
    "101": {"name": "Aifee", "marks": 85},
    "102": {"name": "Nauval", "marks": 92}
}

print(students["102"]["name"])  # Nauval
```

---

## 🗂️ 4. **File Handling**

### 📘 What is File Handling?

File handling lets Python **read and write data** to your computer —
like saving a note in Notepad or reading a text file.

---

### 📄 Opening a File

| Mode  | Meaning                     |
| ----- | --------------------------- |
| `"r"` | Read                        |
| `"w"` | Write (replace old content) |
| `"a"` | Append (add new content)    |

---

### 🔹 Writing to a File

```python
file = open("info.txt", "w")
file.write("Hello, this is my first file!\n")
file.write("I love Python.")
file.close()
```

✅ This will **create** a file named `info.txt`.

---

### 🔹 Reading from a File

```python
file = open("info.txt", "r")
content = file.read()
print(content)
file.close()
```

---

### 🔹 Reading Line by Line

```python
file = open("info.txt", "r")
for line in file:
    print(line.strip())
file.close()
```

---

### 🔹 Using “with” (Best Way)

You don’t need to close the file manually:

```python
with open("info.txt", "a") as f:
    f.write("\nAdding new line safely.")
```

---

## 🔶 5. **Using Python Modules**

### 📘 What is a Module?

A **module** is extra code you can use — like a toolbox for Python.
You “import” it using the `import` keyword.

---

### 🧮 `math` Module

```python
import math

print(math.sqrt(25))   # 5.0
print(math.ceil(4.3))  # 5
print(math.floor(4.8)) # 4
```

---

### 🎲 `random` Module

```python
import random

print(random.randint(1, 10))   # Random number between 1–10
colors = ["red", "blue", "green"]
print(random.choice(colors))   # Pick random color
```

---

### ⏰ `datetime` Module

```python
import datetime

now = datetime.datetime.now()
print(now)   # Shows full date & time
```

Format it nicely:

```python
print(now.strftime("%Y-%m-%d %H:%M:%S"))
```

Output example:

```
2025-10-24 23:45:02
```

---

## 🎯 **Day 4 Summary**

By now you can:

✅ Use **tuples**, **sets**, and **dictionaries**

✅ **Read and write** text files

✅ Use modules like **math**, **random**, and **datetime**

---

## 🧩 **Practice Exercises**

### 🧠 Exercise 1 – Tuple

Create a tuple:

```python
info = ("Ethal", 22, "Bangladesh")
```

* Print each item
* Try changing one (see error)

---

### 🧠 Exercise 2 – Set

Make:

```python
numbers = {1, 2, 2, 3, 4, 4}
```

* Print it (notice duplicates removed)
* Add `5` to it
* Remove `3`

---

### 🧠 Exercise 3 – Dictionary

Make:

```python
book = {"title": "Python 101", "author": "John"}
```

* Add `"year": 2025`
* Change `"author"` to `"Alice"`
* Print all key-value pairs

---

### 🧠 Exercise 4 – File Writing

Ask user for their favorite movie, and write it in a file:

```python
movie = input("Enter your favorite movie: ")
with open("movies.txt", "w") as f:
    f.write(movie)
```

---

### 🧠 Exercise 5 – Random Numbers

Use `random.randint()` to create 5 random numbers between 1–20.

---

### 🧠 Exercise 6 – Date & Time

Print current date in format:

```
Today is Friday, 24 October 2025
```

---
