## Conditionals in Python

### Definition

**Conditionals** are used to make decisions in a program based on conditions.

They allow the program to execute different code depending on whether a condition is **True or False**.

---

## Basic Syntax

```python
if condition:
    # code runs if True
```

---

## `if` Statement

```python
x = 10

if x > 5:
    print("x is greater than 5")
```

---

## `if - else`

```python
x = 3

if x > 5:
    print("Greater")
else:
    print("Smaller")
```

---

## `if - elif - else`

```python
x = 10

if x > 10:
    print("Greater than 10")
elif x == 10:
    print("Equal to 10")
else:
    print("Less than 10")
```

---

|Greater than||
|---|---|
|`<`|Less than|
|`>=`|Greater or equal|
|`<=`|Less or equalComparison Operators|

|Operator|Meaning|
|---|---|
|`==`|Equal|
|`!=`||

---

## Logical Operators

|Operator|Meaning|
|---|---|
|`and`|Both conditions true|
|`or`|At least one true|
|`not`|Opposite condition|

---

## Example (Real Use)

```python
age = int(input("Enter age: "))

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

---

## Key Points

- `if` → check condition
    
- `elif` → check another condition
    
- `else` → default case
    
- Use indentation properly
    

---

## Simple Trick ⭐

👉 **if = decision making**

```python
1. if condition
   elif multiple condition
   else only false   condition.
```
![[Pasted image 20260409094943.png]]