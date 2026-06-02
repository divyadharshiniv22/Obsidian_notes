## `while` Loop – Step-by-Step (Never Forget Method)

### 🧠 Core Formula (Memorize This)

👉 **Initialize → Check → Run → Update → Repeat**

---

## 🔹 Example Code

```python
i = 0

while i < 3:
    print("Hello")
    i += 1
```

---

## 🔍 Step-by-Step Execution

### 1️⃣ Initialize

```python
i = 0
```

👉 Start value

---

### 2️⃣ Check Condition

```python
i < 3   → 0 < 3 → True
```

👉 Enter loop

---

### 3️⃣ Run Code

```python
print("Hello")
```

👉 Output:

```
Hello
```

---

### 4️⃣ Update Value

```python
i += 1   → i = 1
```

---

## 🔁 Repeat Again

### Check:

```python
1 < 3 → True
```

👉 Print → Hello  
👉 Update → i = 2

---

### Check Again:

```python
2 < 3 → True
```

👉 Print → Hello  
👉 Update → i = 3

---

### Final Check:

```python
3 < 3 → False
```

❌ Loop stops

---

## ✅ Final Output

```
Hello
Hello
Hello
```

---

## 🔴 IMPORTANT (Don’t Forget)

👉 If you forget this line:

```python
i += 1
```

⚠️ Loop becomes **infinite**

---

## 🧠 Super Easy Memory Trick

👉 **3 Words Rule**

1. **Start** → `i = 0`
    
2. **Stop Condition** → `i < 3`
    
3. **Step** → `i += 1`
    

---

## 🔑 Golden Rule

👉 **“No update → no stop → infinite loop”**

---

## 💡 Visual Thinking

```
Start → Check → Print → Increase → Check → ... → Stop
```

---

## ⭐ Final Shortcut

👉 **while = repeat until False**