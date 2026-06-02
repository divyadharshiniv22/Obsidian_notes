what is name error and what is value error

# NameError vs ValueError in Python

Both are exceptions in Python, but they happen for different reasons.

---

# 1. NameError

## Definition

`NameError` occurs when Python cannot find a variable or function name.

---

## Example

```
print(age)
```

Output:

```
NameError: name 'age' is not defined
```

### Why?

Because variable `age` was never created.

---

## Correct Version

```
age = 25print(age)
```

---

# Common Reasons for NameError

|Cause|Example|
|---|---|
|Variable not defined|`print(x)`|
|Wrong spelling|`pritn()`|
|Using variable before creation|`print(name)` before `name = "Divya"`|

---

# Example with try-except

```
try:    print(city)except NameError:    print("Variable not found")
```

---

# 2. ValueError

## Definition

`ValueError` occurs when:

- the data type is correct
- but the value is invalid

---

## Example

```
number = int("hello")
```

Output:

```
ValueError: invalid literal for int()
```

### Why?

`int()` expects a number like:

```
"10"
```

but `"hello"` is not a valid numeric value.

---

# Another Example

```
import mathprint(math.sqrt(-1))
```

Output:

```
ValueError: math domain error
```

---

# Example with try-except

```
try:    x = int(input("Enter number: "))except ValueError:    print("Please enter valid number")
```

---

# Difference Between NameError and ValueError

|NameError|ValueError|
|---|---|
|Variable/function name not found|Invalid value|
|`print(age)`|`int("hello")`|
|Name missing|Value wrong|

---

# Easy Understanding

## NameError

```
Python says:"I don't know this variable name."
```

---

## ValueError

```
Python says:"The value you gave is invalid."
```

---

# Real-Life Analogy

|Error|Analogy|
|---|---|
|NameError|Calling a person who is not in the room|
|ValueError|Giving wrong answer in correct format|

---

# Short Definitions

```
NameError → variable/function name not found
```

```
ValueError → correct type but invalid value
```