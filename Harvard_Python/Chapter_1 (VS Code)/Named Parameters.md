## Positional vs Named Arguments (Clear Explanation)

### 🔹 Positional Arguments

**Definition**  
Values are passed to a function based on their **position (order)**.

```python
print("Hello", "David")
```

- First value → goes to first position
    
- Second value → goes to second position
    

👉 Order **matters**

---

### 🔹 Named Arguments (Keyword Arguments)

**Definition**  
Values are passed using **parameter names**, not position.

```python
print("Hello", "David", sep=", ")
```

- `sep=", "` → explicitly sets the separator
    
- Python knows where to apply it because of the **name**
    

👉 Order **does NOT matter**

---

## 🔹 Key Difference

| Type       | Based On       | Order Important? |
| ---------- | -------------- | ---------------- |
| Positional | Position       | ✅ Yes            |
| Named      | Parameter name | ❌ No             |

---

## 🔹 Important Rule

👉 **Positional arguments must come before named arguments**

✅ Correct:

```python
print("Hello", "David", sep=", ")
```

❌ Wrong:

```python
print(sep=", ", "Hello", "David")
```

---

## 🔹 Simple Trick (Exam Shortcut ⭐)

👉 **“Position = order matters, Name = order doesn’t matter”**

---

## 🔹 Real Example (Understanding Clearly)

```python
print("A", "B", "C", sep="-", end="!")
```

**Output**

```
A-B-C!
```

- `"A", "B", "C"` → positional
    
- `sep="-"` → named
    
- `end="!"` → named
    

---

## 🔹 Why Use Named Arguments?

- Makes code **easy to read**
    
- Gives **more control**
    
- Avoids confusion in large functions
    

---

## 🔹 Final Summary

- Positional → follow order
    
- Named → use `parameter=value`
    
- Use both together carefully
    
- Always place **positional first**