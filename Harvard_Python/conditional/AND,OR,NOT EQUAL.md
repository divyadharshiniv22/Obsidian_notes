## Logical Operators: `and`, `or`, `not` (Simple Explanation)

These are used in **conditionals** to combine or modify conditions.

---

## 🔹 `and` (Both must be True)

👉 **Condition is True only if BOTH are True**

```python
x = 10

if x > 5 and x < 15:
    print("True")
```

✔️ True (because both conditions are true)

❌ If one is False → whole condition is False

### Simple idea:

👉 **and = BOTH**

---

## 🔹 `or` (At least one True)

👉 **Condition is True if ANY ONE is True**

```python
x = 10

if x < 5 or x < 15:
    print("True")
```

✔️ True (second condition is True)

❌ Only False if BOTH are False

### Simple idea:

👉 **or = ANY ONE**

---

## 🔹 `not` (Reverse)

👉 **Changes True → False, False → True**

```python
x = 10

if not x > 5:
    print("True")
```

❌ Output will NOT print (because condition becomes False)

### Simple idea:

👉 **not = opposite**

---

## 🔹 Quick Truth Table

|A|B|A and B|A or B|
|---|---|---|---|
|True|True|True|True|
|True|False|False|True|
|False|True|False|True|
|False|False|False|False|

---

## 🔹 Real Example

```python
age = 20

if age > 18 and age < 60:
    print("Working age")
```

---

## 🔹 Key Points

- `and` → both conditions must be True
    
- `or` → at least one True
    
- `not` → reverses condition
    

---

## ⭐ Super Simple Trick

👉 **and = BOTH**  
👉 **or = ANY ONE**  
👉 **not = OPPOSITE**