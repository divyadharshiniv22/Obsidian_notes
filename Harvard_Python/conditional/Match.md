![[Pasted image 20260418105451.png]]


![[Pasted image 20260418110143.png]]
-> == MEANS -  EQUAL , = MEANS - ASSIGNMENT OPERATOR.

![[Pasted image 20260418113230.png]]
using match , use case 

## Why “match = clean multiple comparisons” (How it works)

### ❌ Without `match` (repetitive)

```python
name = input("Name: ")

if name == "Harry":
    print("Gryffindor")
elif name == "Hermione":
    print("Gryffindor")
elif name == "Ron":
    print("Gryffindor")
elif name == "Draco":
    print("Slytherin")
else:
    print("Who?")
```

👉 Problem:

- Repeating `name ==` again and again
    
- Longer and less readable
    

---

## ✅ With `match` (clean)

```python
name = input("Name: ")

match name:
    case "Harry" | "Hermione" | "Ron":
        print("Gryffindor")
    case "Draco":
        print("Slytherin")
    case _:
        print("Who?")
```

---

## 🔍 What Changed?

### 1. No Repetition

👉 `match name:` → written once  
👉 No need for `name ==` everywhere

---

### 2. Grouping Values

```python
case "Harry" | "Ron":
```

👉 Multiple values handled in **one line**

---

### 3. Clear Structure

👉 Looks like a decision table:

- Case 1 → Gryffindor
    
- Case 2 → Slytherin
    
- Default → Who?
    

---

### 4. Easier to Read

👉 You can quickly see:

- what is being checked
    
- what happens for each value
    

---

## 🧠 Simple Comparison

|`if-elif`|`match`|
|---|---|
|Repeated checks|One check|
|Long code|Short code|
|Hard to scan|Easy to scan|

---

## 🔑 Key Idea

👉 `match` checks **one variable once**  
👉 `case` lists all possible values

---

## ⭐ Simple Trick

👉 **“One match → many cases”**