Reprompting means:

> asking again with a new or corrected prompt when the previous response or input was wrong, incomplete, or unclear.

while True:
    try:
        x = int(input("What is x? "))
    except ValueError:
        print("x is not an integer")
    else:
        break


**pass**

# Why Do We Use `pass`?

We use `pass` because Python does not allow empty blocks of code.

`pass` acts as a temporary placeholder.

---

# Main Reason

Python expects some code inside:

- `if`
- `for`
- `while`
- `function`
- `class`
- `try`

If nothing is written, Python throws an error.

---

# Example Without `pass`

❌ Wrong

```
if True:
```

Output:

```
IndentationError
```

Because block is empty.

---

# Example With `pass`

✅ Correct

```
if True:    pass
```

Now Python is satisfied.

---

# Real Purpose of `pass`

`pass` is used when:

- code will be added later
- block should remain empty temporarily
- structure is needed now
- avoiding syntax errors

---

# Real Example 1 — Function Placeholder

```
def login():    pass
```

Meaning:

```
"I will write login code later."
```

---

# Real Example 2 — Empty Class

```
class Student:    pass
```

Creates empty class temporarily.

---

# Real Example 3 — Planning Project Structure

```
def payment():    passdef logout():    passdef signup():    pass
```

Developer creates structure first and writes logic later.

---

# Important Understanding

`pass` is NOT for functionality.

It is for:

✅ syntax correctness  
✅ placeholders  
✅ future code development

---

# Why `pass` in Your Loop Did Nothing

```
if i == 5:    pass
```

means:

```
"When i is 5, do nothing."
```

So loop continued normally.

---

# Difference Between `pass`, `break`, and `continue`

| Keyword    | Meaning                |
| ---------- | ---------------------- |
| `pass`     | Do nothing             |
| `break`    | Stop loop completely   |
| `continue` | Skip current iteration |

---

# Easy Real-Life Analogy

```
pass = empty reserved space
```

Example:

```
You leave blank page in notebook to write later.
```

---

# Short Definition

```
pass is used as a placeholder when Python needs a statement but no action is required.
```