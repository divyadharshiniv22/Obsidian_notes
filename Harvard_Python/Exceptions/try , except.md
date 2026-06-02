# Python `try` and `except`

## What is `try`?

`try` is used to write **risky code** that may cause an error.

Python will first execute the code inside the `try` block.

```
try:    x = int(input("Enter number: "))
```

---

## What is `except`?

`except` is used to **handle errors** that happen inside the `try` block.

Instead of stopping the program, Python runs the code inside `except`.

```
except ValueError:    print("Invalid input")
```

---

# Basic Syntax

```
try:    # risky codeexcept:    # error handling code
```

---

# Why We Use `except`

We use `except` to:

- prevent program crashes
- handle errors safely
- show user-friendly messages
- continue program execution

---

# Where We Use `except`

We use `except` when code may produce errors.

## Common Situations

|Situation|Possible Error|
|---|---|
|User input|`ValueError`|
|Division|`ZeroDivisionError`|
|File opening|`FileNotFoundError`|
|List indexing|`IndexError`|
|Wrong data type|`TypeError`|

---

# Example 1 — User Input

```
try:    age = int(input("Enter age: "))except ValueError:    print("Please enter numbers only")
```

### Explanation

If user enters:

```
hello
```

Python cannot convert `"hello"` into integer.

So:

```
ValueError
```

occurs.

`except ValueError` catches the error.

---

# Example 2 — Division

```
try:    result = 10 / 0except ZeroDivisionError:    print("Cannot divide by zero")
```

---

# Example 3 — List Index

```
numbers = [1, 2, 3]try:    print(numbers[5])except IndexError:    print("Index does not exist")
```

---

# Flow of Execution

```
try block runs       ↓Error occurs?   ↓          ↓ No          Yes ↓            ↓continue    except block runs
```

---

# Real-Life Analogy

```
try     → Try doing somethingexcept  → Handle the problem if it fails
```

Example:

```
Try withdrawing money from ATMIf wrong PIN → show error message
```

---

# Important Rule

`except` cannot be used without `try`.

❌ Wrong

```
except:    print("Error")
```

✅ Correct

```
try:    print(10 / 0)except:    print("Error")
```

---

# Multiple `except` Blocks

```
try:    x = int(input("Enter number: "))    print(10 / x)except ValueError:    print("Invalid number")except ZeroDivisionError:    print("Cannot divide by zero")
```

---

# Short Notes

## `try`

- contains risky code
- code that may cause error

## `except`

- catches the error
- handles the error safely

---

# One-Line Definition

```
try  → runs risky codeexcept → handles errors without crashing the program
```