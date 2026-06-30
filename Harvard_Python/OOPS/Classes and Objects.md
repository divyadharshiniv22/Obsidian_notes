	
Imagine a **class** as a **blueprint** and an **object** as the real thing created from that blueprint.

### Correct Understanding

A **class** is a blueprint/template.

For example, a mobile phone company has one design (class):

```
Mobile Phone- Brand- Color- Features
```

From this one design, they can create many phones (objects):

```
Phone 1 → Samsung, BlackPhone 2 → Apple, WhitePhone 3 → OnePlus, Blue
```

Here:

- **Class** = Mobile Phone blueprint
- **Objects** = Phone 1, Phone 2, Phone 3

---

### Your Code

```
class Phone:    def __init__(self, brand, color):        self.brand = brand        self.color = color
```

Create objects:

```
phone1 = Phone("Samsung", "Black")phone2 = Phone("Apple", "White")
```

---

### What is `__init__()`?

`__init__()` is called automatically when an object is created.

```
phone1 = Phone("Samsung", "Black")
```

Python internally does:

```
Phone.__init__(phone1, "Samsung", "Black")
```

So:

```
self = phone1
brand = "Samsung"
color = "Black"
```

Then:

```
self.brand = brandself.color = color
```

stores the values inside `phone1`.

### Interview Version

> A class is a blueprint or template. Objects are created from the class. The `__init__()` method initializes the object's attributes, and `self` stores the values inside the current object. For example, one `Phone` class can be used to create many phone objects with different brands and colors


The classes and object :

### `int` Class

Used for integers (whole numbers).

```
x = 10print(type(x))
```

Output:

```
<class 'int'>
```

Meaning:

> `10` is an object created from the `int` class.

---

### `str` Class

Used for text (strings).

```
name = "Divya"print(type(name))
```

Output:

```
<class 'str'>
```

### `int` Class

Used for integers (whole numbers).

```
x = 10
print(type(x))
```

Output:

```
<class 'int'>
```

Meaning:

> `10` is an object created from the `int` class.

---

### `str` Class

Used for text (strings).

```
name = "Divya"
print(type(name))
```

Output:

```
<class 'str'>
```

### Easy Memory Trick

```
dict      -> Class
dict()    -> Object
Student      -> Class
Student()    -> Object
```

That's why instructors often write:

```
type(dict())
```


