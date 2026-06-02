
---

## 🔹 Indentation

### Definition

**Indentation** means adding spaces (or tabs) at the beginning of a line to define a **block of code**.

Python uses indentation instead of `{}` (like other languages).

---

### Example

```python
if True:
    print("Hello")
```

👉 The indented line belongs to the `if` block

---

### ❌ Wrong Example

```python
if True:
print("Hello")
```

👉 This causes **IndentationError**

---

## 🔹 Colon `:`

### Definition

A **colon `:`** is used to **start a block of code**.

---

### Example

```python
x = 10

if x > 5:
    print("Greater")
```

👉 `:` tells Python → “start block here”

---

## 🔹 Together Example

```python
x = int(input("Enter number: "))

if x > 0:
    print("Positive")
else:
    print("Not positive")
```

---

## 🔹 Key Points

- Indentation → defines block
    
- `:` → starts block
    
- Both are **mandatory in Python**
    

---

## ⭐ Simple Trick

👉 **: = start block**  
👉 **Indent = inside block**



## Chaining Comparison Operators in Python

### Definition

**Chaining comparison operators** means combining multiple comparisons in a single line.

👉 Python evaluates them **left to right**

---

## Basic Syntax

```python
a < b < c 
```

👉 This is equivalent to:

```python
(a < b) and (b < c)
```

---

## Example

```python
x = 40

if 30 < x < 50:
    print("x is between 30 and 50")
```

**Output**

```
x is between 30 and 50
```

---

## How It Works

```python
30 < x < 50
```

👉 Python checks:

- `30 < x` → True
    
- `x < 50` → True
    

👉 Final result → **True**

---

## Another Example

```python
x = 10

if 5 < x < 8:
    print("Yes")
else:
    print("No")
```

👉 Output:

```
No
```

---

## ❗ Important Rule

👉 All conditions must be **True**

---

## ❌ Confusing Example (Avoid)

```python
x < 50 != x <= 30
```

👉 Python reads it as:

```python
(x < 50) and (50 != x) and (x <= 30)
```

👉 Hard to understand → avoid this style

---

## ✅ Best Practice

✔️ Use chaining for **ranges**

```python
10 < x < 20
```

✔️ Use `and` for clarity

```python
x > 10 and x < 20
```

---

## Key Points

- Chaining = multiple comparisons in one line
    
- Works like `and` between conditions
    
- Best for **range checking**
    
- Avoid complex chains
    

---

## Simple Trick ⭐

👉 **“Chain = range check”**



==THIS CONDITION IS WORK FOR AND ONLY . NOT EQUAL,  OR IT WON'T WORK.==