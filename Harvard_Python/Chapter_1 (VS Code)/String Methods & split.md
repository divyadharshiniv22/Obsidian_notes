## String Methods in Python

### Definition

**String methods** are built-in functions used to **modify, clean, or analyze strings**.

They are used with **dot notation**:

```python
text.method()
```

---

## Common String Methods

### 1. Case Conversion

```python
name = "david"

print(name.upper())      # DAVID
print(name.lower())      # david
print(name.capitalize()) # David
print(name.title())      # David
```

---

### 2. Removing Spaces

```python
text = "   David   "

print(text.strip())   # both sides
print(text.lstrip())  # left side
print(text.rstrip())  # right side
```

---

### 3. Replacing Text

```python
text = "Hello David"
print(text.replace("David", "John"))
```

---

### 4. Finding Text

```python
text = "Hello David"
print(text.find("David"))   # position index
```

---

### 5. Checking Content

```python
text = "David123"

print(text.isalpha())   # False
print(text.isdigit())   # False
print(text.isalnum())   # True
```

---

### 6. Splitting and Joining

```python
text = "apple,banana,grape"
print(text.split(","))   # ['apple', 'banana', 'grape']

words = ["Hello", "David"]
print(" ".join(words))   # Hello David
```

---

## Real Example

```python
name = input("What's your name? ")
name = name.strip().title()
print(f"Hello, {name}")
```

👉 Cleans input and formats nicely

---

## Key Points

- Use **dot (****`.`****)** to call methods → `string.method()`
    
- Strings are **immutable** (original does not change)
    
- Methods return a **new string**
    
- Methods can be **chained**
    

---

## Simple Trick ⭐

👉 **“dot = do something to string”**


## `split()` in Python

### Definition

`split()` is a **string method** used to **break a string into parts** and return them as a **list**.

---

## Basic Syntax

```python
string.split(separator)
```

- `separator` → the character used to split the string
    
- Default separator → **space**
    

---

## Examples

### 1. Default Split (space)

```python
text = "Hello David"
print(text.split())
```

**Output**

```
['Hello', 'David']
```

---

### 2. Split by Comma

```python
text = "apple,banana,grape"
print(text.split(","))
```

**Output**

```
['apple', 'banana', 'grape']
```

---

### 3. Split by Custom Character

```python
text = "A-B-C"
print(text.split("-"))
```

**Output**

```
['A', 'B', 'C']
```

---

## Important Points

- Returns a **list**
    
- Does not change the original string
    
- Default separator is **space**
    
- Can use any character as separator
    

---

## Real Example

```python
name = input("Enter full name: ")
words = name.split()
print(words)
```

👉 Converts user input into a list of words

---

## Simple Trick ⭐

👉 **split = break string into list**