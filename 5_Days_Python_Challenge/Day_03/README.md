---

# 🐍 **DAY 3 – Loops, Lists, and Strings**

---

## 🧠 **1. What Are Loops?**

Loops are used to **execute a block of code repeatedly** — instead of writing the same line again and again.

Think of a loop as an automatic “repeat button” for your code.

### 🔁 Real-Life Example:

> You want to print your name 5 times.
> Instead of:
>
> ```python
> print("Aifee")
> print("Aifee")
> print("Aifee")
> print("Aifee")
> print("Aifee")
> ```
>
> You can use:
>
> ```python
> for i in range(5):
>     print("Aifee")
> ```

---

## **2. for Loops**

### 🔹 Definition:

A `for` loop is used to iterate (go through) items in a **sequence** — like a list, string, or range of numbers.

---

### 🧩 **Syntax:**

```python
for variable in sequence:
    # Code block to execute
```

### 🧠 **How It Works:**

* Takes the **first item** from the sequence
* Assigns it to the variable
* Runs the code block
* Repeats for every item in the sequence

---

### 🔸 Example 1: Looping through a Range

```python
for i in range(1, 6):
    print("Number:", i)
```

🖥️ Output:

```
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5
```

---

### 🔸 Example 2: Looping through a List

```python
colors = ["red", "green", "blue"]
for color in colors:
    print("Color:", color)
```

🧠 The variable `color` takes one value from the list each time.

---

### 🔸 Example 3: Looping through a String

```python
for ch in "Python":
    print(ch)
```

🖥️ Output:

```
P
y
t
h
o
n
```

---

## **3. while Loops**

### 🔹 Definition:

A `while` loop repeats **as long as a condition remains True**.

---

### 🧩 **Syntax:**

```python
while condition:
    # Code block
```

If the condition is False, the loop stops.

---

### 🔸 Example 1:

```python
count = 1
while count <= 5:
    print("Count:", count)
    count += 1  # increment to avoid infinite loop
```

🖥️ Output:

```
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
```

---

### ⚠️ Infinite Loop Warning:

If you forget to update your condition, the loop runs forever.

```python
while True:
    print("This will run forever!")
```

Stop it manually (Ctrl + C in terminal).

---

## **4. Loop Control Statements**

Sometimes, you want more control inside loops — skip items, stop early, or leave placeholders.

| Keyword    | Purpose                            | Example               |
| ---------- | ---------------------------------- | --------------------- |
| `break`    | Exit the loop completely           | `if i == 5: break`    |
| `continue` | Skip current iteration             | `if i == 3: continue` |
| `pass`     | Do nothing (used as a placeholder) | `if i == 2: pass`     |

---

### 🔸 Example: `break`

```python
for i in range(1, 6):
    if i == 4:
        break
    print(i)
```

🖥️ Output:

```
1
2
3
```

---

### 🔸 Example: `continue`

```python
for i in range(1, 6):
    if i == 3:
        continue  # skip 3
    print(i)
```

🖥️ Output:

```
1
2
4
5
```

---

### 🔸 Example: `pass`

```python
for i in range(1, 4):
    if i == 2:
        pass  # placeholder
    print(i)
```

---

## **5. Working with Strings**

Strings are **sequences of characters**, so they behave like lists.

---

### **5.1 Indexing**

Each character in a string has a position (index):

```
 P   y   t   h   o   n
 0   1   2   3   4   5
```

```python
text = "Python"
print(text[0])   # 'P'
print(text[5])   # 'n'
```

Negative indices count from the end:

```python
print(text[-1])  # 'n'
print(text[-2])  # 'o'
```

---

### **5.2 Slicing**

Extract parts of a string:

```python
word = "Programming"
print(word[0:4])   # 'Prog'
print(word[:6])    # 'Progra'
print(word[3:])    # 'gramming'
print(word[-3:])   # 'ing'
```

---

### **5.3 Common String Methods**

| Method       | Purpose                     | Example                                   | Output            |
| ------------ | --------------------------- | ----------------------------------------- | ----------------- |
| `.upper()`   | Convert to uppercase        | `"hello".upper()`                         | `'HELLO'`         |
| `.lower()`   | Convert to lowercase        | `"HELLO".lower()`                         | `'hello'`         |
| `.find()`    | Find index of substring     | `"Python".find("th")`                     | `2`               |
| `.replace()` | Replace text                | `"I love Java".replace("Java", "Python")` | `'I love Python'` |
| `.split()`   | Split string into list      | `"a,b,c".split(",")`                      | `['a', 'b', 'c']` |
| `.join()`    | Join list into string       | `",".join(['a', 'b', 'c'])`               | `'a,b,c'`         |
| `.strip()`   | Remove spaces               | `" hello ".strip()`                       | `'hello'`         |
| `.count()`   | Count substring occurrences | `"banana".count("a")`                     | `3`               |

---

### **5.4 Looping Over Strings**

```python
name = "Aifee"
for ch in name:
    print(ch, end=" ")
```

🖥️ Output:

```
A i f e e
```

---

## **6. Lists**

### 🔹 Definition:

Lists are **mutable sequences** used to store multiple items in a single variable.

```python
fruits = ["apple", "banana", "cherry"]
```

---

### **6.1 Creating Lists**

```python
numbers = [1, 2, 3, 4, 5]
names = ["Aifee", "Nauval", "Pringgo"]
mixed = [10, "Python", True, 5.6]
empty = []
```

---

### **6.2 Accessing Elements**

```python
print(numbers[0])   # 1
print(numbers[-1])  # 5
```

---

### **6.3 Modifying Lists**

| Method          | Description        | Example                     | Result                                    |
| --------------- | ------------------ | --------------------------- | ----------------------------------------- |
| `.append(x)`    | Add element at end | `fruits.append("orange")`   | `['apple', 'banana', 'cherry', 'orange']` |
| `.insert(i, x)` | Insert at index    | `fruits.insert(1, "mango")` | `['apple', 'mango', 'banana', 'cherry']`  |
| `.remove(x)`    | Remove by value    | `fruits.remove("banana")`   | `['apple', 'mango', 'cherry']`            |
| `.pop(i)`       | Remove by index    | `fruits.pop(2)`             | Removes the 3rd item                      |
| `.sort()`       | Sort the list      | `numbers.sort()`            | `[1,2,3,4,5]`                             |
| `.reverse()`    | Reverse order      | `numbers.reverse()`         | `[5,4,3,2,1]`                             |

---

### **6.4 List Slicing**

```python
nums = [10, 20, 30, 40, 50]
print(nums[1:4])  # [20, 30, 40]
print(nums[:3])   # [10, 20, 30]
print(nums[2:])   # [30, 40, 50]
```

---

### **6.5 Looping Through Lists**

```python
for fruit in fruits:
    print(fruit)
```

Using index:

```python
for i in range(len(fruits)):
    print(i, fruits[i])
```

---

### **6.6 Using the `in` Keyword**

```python
if "banana" in fruits:
    print("Yes, banana is there!")
else:
    print("No banana!")
```

---

## **7. The `range()` Function**

`range()` creates a sequence of numbers — often used in loops.

### **Syntax:**

```python
range(start, stop, step)
```

### Examples:

```python
for i in range(5):
    print(i)   # 0 to 4

for i in range(1, 6):
    print(i)   # 1 to 5

for i in range(0, 10, 2):
    print(i)   # 0, 2, 4, 6, 8
```

---

## 🎯 **DAY 3 GOALS**

By the end of this day, you should be able to:
✅ Use `for` and `while` loops effectively

✅ Control loops with `break`, `continue`, and `pass`

✅ Work with **strings** (indexing, slicing, methods)

✅ Manipulate **lists** (create, modify, slice, iterate)

✅ Use `in` and `range()` for efficient looping

---

## 💻 **Practice Exercises**

### 🔹 **Exercise 1 – Loop Practice**

Print numbers from 1 to 10 using both `for` and `while` loops.

---

### 🔹 **Exercise 2 – Even Numbers**

Use a loop to print even numbers between 1 and 20.

---

### 🔹 **Exercise 3 – Reverse a String**

Ask the user for a string and print its reverse using slicing:

```python
text = input("Enter text: ")
print(text[::-1])
```

---

### 🔹 **Exercise 4 – Word Splitter**

Ask user to enter a sentence, split it into words, and print each word in a new line.

---

### 🔹 **Exercise 5 – List Operations**

Create:

```python
numbers = [5, 10, 15]
```

Then:

* Append 20
* Insert 0 at the beginning
* Remove 10
* Print final list

---

### 🔹 **Exercise 6 – Multiplication Table**

Ask for a number, print its table using a loop:

```python
n = int(input("Enter number: "))
for i in range(1, 11):
    print(f"{n} x {i} = {n * i}")
```

---

### 🔹 **Exercise 7 – Password Loop**

Keep asking for password until correct:

```python
while True:
    pwd = input("Enter password: ")
    if pwd == "Python123":
        print("Access granted!")
        break
    else:
        print("Wrong password, try again.")
```

---

### 🔹 **Exercise 8 – Find the Largest Number**

Given:

```python
nums = [23, 56, 12, 89, 45]
```

Use a loop to find and print the **largest** number manually (without using `max()`).

---
