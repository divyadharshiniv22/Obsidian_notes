
### Definition

**Type conversion** means changing a value from one data type to another.

---

## Why It Is Needed

```
x = input("Enter number: ")
print(x + x)
```

**Output**

```
1010
```

👉 Because `input()` returns a **string**, not a number.

---

## Common Conversion Functions

|Function|Converts To|Example|
|---|---|---|
|`int()`|Integer|`int("10") → 10`|
|`float()`|Decimal|`float("10.5") → 10.5`|
|`str()`|String|`str(10) → "10"`|

---

## Examples

### String → Integer

```
x = int("10")
print(x + 5)
```

**Output**

```
15
```

---

### Integer → String

```
x = 10
print("Value: " + str(x))
```

---

### String → Float

```
price = float("99.99")
print(price)
```

---

## Fixing Input Problem

```
x = int(input("what is x ? "))
y = int(input("what is y ? "))
print(x + y)
```

**Output**

```
11
```

---

## Key Points

- `input()` → always **string**
- Convert using `int()` / `float()` for math
- Use `str()` when combining text + number

---

## Common Mistake

```
"5" + "6"   # "56" (concatenation)
```

```
5 + 6       # 11 (addition)
```

Floating Point Values

## Floating Point Input and Rounding

### Code

```
x = float(input("What's x? "))
y = float(input("What's y? "))

z = round(x + y)

print(z)
```