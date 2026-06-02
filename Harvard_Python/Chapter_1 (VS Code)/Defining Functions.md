## Defining Functions in Python

### Definition

A **function** is a reusable block of code that performs a specific task.

You define a function using the `def` keyword.

---

## Basic Syntax

```python
def function_name():
    # code block
```

---

## Example

```python
def greet():
    print("Hello, World")

greet()
```

**Output**

```
Hello, World
```

---

## Function with Parameters

```python
def greet(name):
    print("Hello,", name)

greet("David")
```

**Output**

```
Hello, David
```

---

## Function with Return Value

```python
def add(x, y):
    return x + y

result = add(5, 3)
print(result)
```

**Output**

```
8
```

---

## Why Use Functions?

- Avoid repeating code
    
- Make code **clean and organized**
    
- Reuse logic multiple times
    

---

## Key Parts of a Function

|Part|Meaning|
|---|---|
|`def`|Defines function|
|`name`|Function name|
|`()`|Parameters|
|`:`|Start of block|
|`return`|Sends value back|

---

## Example (Real Use)

```python
def greet_user():
    name = input("What's your name? ")
    print(f"Hello, {name}")

greet_user()
```

---

## Key Points

- Use `def` to define function
    
- Call function using its name
    
- Can take inputs (**parameters**)
    
- Can return values
    

---

## Simple Trick ⭐

👉 **def = define function**




## `return` in Python

### Definition

The `return` statement is used to **send a value back** from a function to where it was called.

---

## Basic Example

```python
def add(x, y):
    return x + y

result = add(5, 3)
print(result)
```

**Output**

```
8
```

👉 The function calculates and **returns** the value

---

## Without `return`

```python
def add(x, y):
    print(x + y)

result = add(5, 3)
print(result)
```

**Output**

```
8
None
```

👉 Function prints the value but does **not return** it  
👉 So `result` becomes `None`

---

## Key Difference

|`return`|`print`|
|---|---|
|Sends value back|Displays value|
|Can be reused|Cannot reuse|
|Ends function|Continues execution|

---

## Example (Real Use)

```python
def square(n):
    return n * n

value = square(4)
print(value)
```

---

## Multiple Returns

```python
def check(num):
    if num > 0:
        return "Positive"
    else:
        return "Negative"
```

---

## Important Points

- `return` ends the function
    
- You can store returned value in a variable
    
- If no `return`, function returns `None`
    

---

## Simple Trick ⭐

👉 **return = give back value**
