## Loops in Python (Introduction)

### Definition

A **loop** is used to **repeat a block of code multiple times**.

👉 Instead of writing the same code again and again, we use loops.

---

## 🔹 Why Use Loops?

- Avoid repetition
    
- Save time
    
- Make code shorter and cleaner
    

---

## 🔹 Types of Loops

### 1. `while` Loop

👉 Runs **while condition is True**

```python
i = 1

while i <= 5:
    print(i)
    i += 1
```

**Output**

```
1
2
3
4
5
```

---

### 2. `for` Loop

👉 Used to iterate over a sequence

```python
for i in range(1, 6):
    print(i)
```

---

## 🔹 Infinite Loop (⚠️)

```python
while True:
    print("Hello")
```

👉 Runs forever (unless stopped)

---

## 🔹 Loop Control

### `break` → stops loop

```python
for i in range(5):
    if i == 3:
        break
    print(i)
```

---

### `continue` → skip current iteration

```python
for i in range(5):
    if i == 2:
        continue
    print(i)
```

---

## 🔹 Real Example

```python
name = ""

while name == "":
    name = input("Enter your name: ")

print(f"Hello, {name}")
```

---

## 🔑 Key Points

- Loop = repeat code
    
- `while` → condition-based
    
- `for` → sequence-based
    
- Use `break` and `continue` for control
    

---

## ⭐ Simple Trick

👉 **Loop = repeat until condition changes**



## `cat.py` (Simple Loop Program)

### Goal

Print `"meow"` multiple times like a cat 🐱

---

## Basic Version (Manual)

```python
print("meow")
print("meow")
print("meow")
```

👉 Repetition ❌ (not efficient)

---

## Using `for` Loop (Best Way)

```python
for _ in range(3):
    print("meow")
```

👉 Output:

```
meow
meow
meow
```

---

## Using `while` Loop

```python
i = 0

while i < 3:
    print("meow")
    i += 1
```

---

## User Input Version

```python
n = int(input("Number of times: "))

for _ in range(n):
    print("meow")
```

---

## 🔍 Why `_`?

- `_` is used when we **don’t care about the variable**
    
- Just used for looping
    

---

## 🔑 Key Points

- Loops avoid repetition
    
- `for` loop is cleaner than `while` here
    
- `range(n)` → runs `n` times
    

---

## ⭐ Simple Trick

👉 **Loop = repeat "meow" easily**