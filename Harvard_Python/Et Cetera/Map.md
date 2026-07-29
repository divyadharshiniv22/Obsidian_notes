`map()` is a built-in function that applies a given function to every element of an iterable and returns a map object (iterator).
```python
map(function, iterable)

or with multiple iterables:

map(function, iterable1, iterable2)
```
```python
def main():
    yell("this is called cs50") # call the function
def yell(*word): # word is positional argument can store in the tuple 
    uppercased=map(str.upper,word) # map() takes every element in the tuple and applies str.upper.
    print(*uppercased) # give uppercase

if __name__ == "__main__":
    main()
```

# Interview Answer

**Q: Why do we use `map()` in Python?**

**Answer:**  
`map()` is used to apply the same function to every element of an iterable. It helps write shorter, cleaner code and avoids an explicit `for` loop when the same transformation is needed for every item.


# Real-Life Analogy

Imagine a teacher has 5 answer sheets.

```
Divya
Rahul
Anu
Vijay
Priya
```

The teacher stamps **"PASS"** on every sheet.

```
Divya  → PASS
Rahul  → PASS
Anu     → PASS
Vijay   → PASS
Priya   → PASS
```

The teacher performs **the same action** on every item.

`map()` works in the same way: it applies the **same function** to every element.

---

# When should you use `map()`?

Use `map()` when you want to perform **the same operation on every element**.

Examples:

- Convert all names to uppercase.
- Convert a list of strings to integers.
- Double every number.
- Square every number.