# What is Operator Overloading?

### Simple Definition

> **Operator overloading means giving a new meaning or behavior to an existing operator (`+`, `-`, `*`, `==`, etc.) for objects.**

---

# Real Example

Normally:

```
print(10 + 20)
```

Output:

```
30
```

Here,

```
+
```

adds two numbers.

---

Now look at this:

```
print("Hello " + "Divya")
```

Output:

```
Hello Divya
```

Wait...

The same `+` operator is now **joining two strings**, not adding numbers.

So the `+` operator has **different behavior** depending on the type of the operands.

This is **operator overloading**.

# Our Own Class

Suppose we create a class.

```python

class student():

    def __init__(self,name):

        self.name = name

    def __add__(self,other):

        return f'{self.name } {other.name}'

s1 = student("jimmy")

s2 = student("wami")

print(s1+s2)
```

# Common Special Methods

| Operator | Method          |
| -------- | --------------- |
| `+`      | `__add__()`     |
| `-`      | `__sub__()`     |
| `*`      | `__mul__()`     |
| `/`      | `__truediv__()` |
| `==`     | `__eq__()`      |
| `<`      | `__lt__()`      |
| `>`      | `__gt__()`      |
s1 + s2 
↓ 
Python automatically calls 
↓
s1.__add__(s2)