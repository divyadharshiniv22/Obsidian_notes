## Escaping Characters in Python

### Definition

**Escape characters** are used to include special characters inside strings.  
They start with a **backslash `\`**.

---

## Common Escape Characters

|Escape|Meaning|
|---|---|
|`\"`|Double quote|
|`\'`|Single quote|
|`\\`|Backslash|
|`\n`|New line|
|`\t`|Tab space|

---

## Examples

### Quotes inside string

```python
print("He said \"Hello\"")
```

### New line

```python
print("Hello\nDavid")
```

### Tab space

```python
print("Hello\tDavid")
```

### Backslash

```python
print("C:\\Users\\David")
```

---

## Key Points

- Escape character starts with `\`
    
- Used to print special characters
    
- Helps avoid errors with quotes
    
- Common ones: `\"`, `\n`, `\t`, `\\`
    

---

## Simple Trick ⭐

👉 **“\ = special meaning starts”**



## f-Strings in Python

### Definition

**f-Strings (formatted strings)** are a modern and easy way to include variables inside a string.

They start with the letter `f` before the quotes.

---

## Basic Syntax

```
name = "David"
print(f"Hello, {name}")
```

**Output**

```
Hello, David
```

- `{name}` → variable is inserted inside the string

---

## Example with Input

```
name = input("What's your name? ")
print(f"Hello, {name}")
```

---

## Multiple Variables

```
name = "David"
age = 25
print(f"My name is {name} and I am {age} years old")
```

---

## Expressions inside f-Strings

You can even use calculations inside `{}`:

```
print(f"2 + 3 = {2 + 3}")
```

**Output**

```
2 + 3 = 5
```

---

## Why Use f-Strings?

- Clean and readable
- No need for `+` or commas
- Supports variables and expressions
- Best practice in modern Python ⭐

---

## Comparison

```
# Using comma
print("Hello,", name)

# Using +
print("Hello, " + name)

# Using f-string (best)
print(f"Hello, {name}")
```

---

## Key Points

- Start string with `f`
- Use `{}` to insert variables
- Can include expressions inside `{}`

---

## Simple Trick ⭐

👉 **f = format (insert values inside string easily)**