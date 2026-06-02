## Modulo Operator (`%`) in Python

### Definition

The **modulo operator `%`** gives the **remainder** after division.

---

## Basic Syntax

```python
a % b
```

👉 Returns the **remainder** when `a` is divided by `b`

---

## Examples

```python
print(10 % 3)   # 1
print(20 % 5)   # 0
print(7 % 2)    # 1
```

---

## Explanation

```python
10 % 3
```

👉 10 ÷ 3 = 3 remainder **1**

---

## Common Uses

### 1. Check Even or Odd

```python
x = 4

if x % 2 == 0:
    print("Even")
else:
    print("Odd")
```

---

### 2. Divisibility Check

```python
x = 15

if x % 5 == 0:
    print("Divisible by 5")
```

---

### 3. Loop Patterns

```python
for i in range(1, 6):
    print(i % 2)
```

---

## Key Points

- `%` → gives **remainder**
    
- If result = 0 → number is **divisible**
    
- Commonly used for **even/odd checks**
    

---

## Simple Trick ⭐

👉 **% = remainder**




## Boolean in Python

### Definition

A **Boolean** is a data type that has only two values:

👉 `True`  
👉 `False`

---

## Basic Examples

```python
print(True)
print(False)
```

---

## Boolean from Comparisons

```python
print(5 > 3)    # True
print(10 == 5)  # False
print(7 != 2)   # True
```

👉 Comparisons always return **True or False**

---

## Using Boolean in `if`

```python
x = 10

if x > 5:
    print("True")
```

👉 Condition must be **Boolean**

---

## Boolean with Logical Operators

```python
print(True and False)  # False
print(True or False)   # True
print(not True)        # False
```

---

## Boolean from Values

```python
bool(1)     # True
bool(0)     # False
bool("")    # False
bool("Hi")  # True
```

---

## Key Points

- Boolean has only **True / False**
    
- Used in **conditions (if statements)**
    
- Result of comparisons is Boolean
    
- Works with `and`, `or`, `not`
    

---

## Simple Trick ⭐

👉 **Boolean = True or False**